<template>
    <div class="bigCard" ref="bigCard">
        <div class="bigCard-content">
            <div class="bigCard-content-text">
                <p>Discover your next favorite game on Jules. Browse through our wide collection of games - from the most
                    popular titles to hidden indie gems. Enjoy competitive prices and a user-friendly interface.</p>
                <div class="bigCard-content-button">
                <div class="shop">Go To Store</div>
                    <p style="margin-left: 15px;font-weight: 200;">Watch Beta Demo --></p>
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
        // Set the initial rotation of the card to almost flat
        gsap.set(this.$refs.bigCard, { transformPerspective: 1000, rotationX: 85 });

        // Animate the card to flip up when it enters the view
        gsap.to(this.$refs.bigCard, {
            rotationX: 0,
            scrollTrigger: {
                trigger: this.$refs.bigCard,
                start: 'bottom bottom', // Start the animation when the bottom of the card is at the bottom of the viewport
                toggleActions: 'play none none none'
            }
        });
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
}

.shop:hover {
    background: rgba(217, 217, 217, 0.35);
    cursor: pointer;
}

</style>