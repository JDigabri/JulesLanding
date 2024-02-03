<template>
    <div class="bigCard" ref="bigCard">
        <div class="bigCard-content">
            <div class="bigCard-content-text">
                <p>Discover your next favorite game on Jules. Browse through our wide collection of games - from the most
                    popular titles to hidden indie gems. Enjoy competitive prices and a user-friendly interface.</p>
                <div class="bigCard-content-button">
                <a href = "https://jules.gg" class="shop">Go To Store</a>
                    <a href="https://www.youtube.com/watch?v=jHVc6r6S4t8&feature=youtu.be" style="margin-left: 15px;font-weight: 200; color: white; text-decoration: none;">Watch Beta Demo --></a>
                </div>
            </div>

            <div class = 'bigImg'> </div>
        </div>
    </div>
</template>

<script>
import { gsap } from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';

gsap.registerPlugin(ScrollTrigger);

export default {
    name: 'BigCard', // replace with your component name

    mounted() {
        document.body.style.overflowX = 'hidden';

        // Set the initial rotation of the card to almost flat

        // Use ScrollTrigger's matchMedia method to control the animation based on the viewport width
        ScrollTrigger.matchMedia({
            // When the viewport is wider than 1100 pixels, the following rules will apply
            "(min-width: 1101px)": () => {
                // Register the ScrollTrigger animation
                gsap.set(this.$refs.bigCard, { transformPerspective: 1000, rotationX: 85 });

                gsap.to(this.$refs.bigCard, {
                    rotationX: 0,
                    scrollTrigger: {
                        trigger: this.$refs.bigCard,
                        start: 'bottom bottom', // Start the animation when the bottom of the card is at the bottom of the viewport
                        toggleActions: 'play none none none',
                    }
                });
            },
            // All other viewport sizes (viewport width is 1100 pixels or less)
            "all": () => {
                // You can define alternate animations or simply do nothing
            },
        });
    },
    beforeDestroy() {
        // Clean up by killing ScrollTriggers to prevent memory leaks
        ScrollTrigger.getAll().forEach(trigger => trigger.kill());

        // Re-enable horizontal scrollbar when the component is destroyed
        document.body.style.overflowX = '';
    }
}
</script>


<style scoped>
.bigCard {
    width: 900px;
    height: 300px;
    flex-shrink: 0;
    border-radius: 10px;
    background: linear-gradient(245deg, #BDCFFC 32.08%, #9E77DA 67.06%);
    box-shadow: 0px 4px 24px 7px rgba(0, 0, 0, 0.25);
    position: absolute;
    margin-top: 100px;
    z-index: 55;
    will-change: tramform;
}
.bigCard-content {
    height: 100%;

    display: flex;
    flex-direction: row;
}
.bigImg{
    background-image: url('../assets/storesmall.png');
    width: 450px;
    height: 270px;
    flex-shrink: 0;
    background-repeat: no-repeat;
    background-size: 100%;
    margin-left: auto;
    margin-top: auto;
    border-radius: 20px 0px 10px 0px;


}
.bigCard-content-text {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 35px;
    color: #FFF;
    font-family: Inter;
    font-size: 20px;
    font-style: normal;
    font-weight: 200;
    line-height: normal;
}
.bigCard-content-button{
    display: flex;
    align-items: center;
    margin-top: 20px;
    width: 100%;
    color: #FFF;
    text-align: center;
    font-family: Inter;
    font-size: 16px;
    font-style: normal;
    font-weight: 200;
    line-height: normal;
}
.bigCard-content-button p{
    transition: all 0.3s ease-in-out;

}
.bigCard-content-button p:hover{
    cursor: pointer;
    color: #BDCFFC;
}
.shop {
    transition: all 0.3s ease-in-out;

    border-radius: 25px;
    border: 2px solid rgba(255, 255, 255, 0.35);
    background: rgba(217, 217, 217, 0.00);
    width: 124px;
    height: 44px;
    flex-shrink: 0;
    color: #FFF;
    text-align: center;
    font-family: Inter;
    font-size: 16px;
    font-style: normal;
    font-weight: 200;
    line-height: normal;
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;

}

.shop:hover {
    background: rgba(217, 217, 217, 0.35);
    cursor: pointer;
}


@media screen and (max-width: 900px){
    .bigCard{
        width: 90vw;
    }
    .bigCard-content-text{
        font-size: 15px;

    }
    .bigCard-content-button{
        font-size: 11px;
    }
}

@media screen and (max-width: 800px){
    .bigCard{
        width: 90vw;
        height: 500px;
    }
    .bigCard-content{
        flex-direction: column;
        align-items: center;
    }
    .bigCard-content-text{
        width: 100%;
        font-size: 15px;
        padding: 25px;
    }
    .bigCard-content-text p{
        text-shadow: 0px 0px 4px rgba(0, 0, 0, 0.4);        
    }
    .bigCard-content-button{
        width: 100%;
        height: 50%;
        font-size: 11px;
    }
    .bigImg{
        width: 90%;
        border-radius: 0px 0px 10px 10px;
        align-self: flex-end;
        margin-top: auto;
    }
}

@media screen and (max-width: 550px){
    .bigImg{
        width: 100%;
        border-radius: 0px 0px 10px 10px;
        align-self: flex-end;
        margin-top: auto;
        background-size: 150% 130%;
    }
    .bigCard-content-text{
        font-size: 15px;
        padding: 25px;
    }
}
</style>