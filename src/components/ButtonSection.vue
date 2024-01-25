<template>
    <div class="podcont">
        <div class="podsTop">
            <div class="pod">
                <div class="circle"><img src = "../assets/game.png" /> <img src = "../assets/game.png" style="position: absolute; filter: blur(7px);" /></div>
                <div class="pod-content">
                    <h1>A World of Games at Your Fingertips</h1>
                    <p>Enjoy an immersive, diverse range of games in our all-in-one platform. Experience the thrill of gaming as we continually integrate new and popular titles. Enjoy a seamless, gamer-first experience.</p>
                </div>
            </div>
            <div class="podr">
                <div class="circle"><img src= "../assets/market.png"/> <img src= "../assets/market.png" style="position: absolute; filter: blur(7px);"/></div>
                <div class="pod-content">
                    <h1>Unchain Your Gaming Potential</h1>
                    <p>Don't let unplayed games limit your gaming potential. Jules empowers you to breathe new life into your unused games by selling them to others in our secure, easy-to-use marketplace. It's not just about decluttering your library, it's about passing the fun forward.</p>
                </div>
            </div>
        </div>
        <div class="podsBottom">
            <div class="pod">
                <div class="circle"><img src="../assets/money.png"/> <img src="../assets/money.png" style="position: absolute;filter: blur(7px);"/></div>
                <div class="pod-content">
                    <h1>Unleash the Value of Your Unplayed Games</h1>
                    <p>Turn your unplayed games into real money. At Jules, we offer the unique opportunity to sell your games and in-game items securely to other players. It's time to turn your unplayed games into new opportunities.</p>
                </div>
            </div>
            <div class="podr">
                <div class="circle"><img src = "../assets/transfer.png"/> <img src = "../assets/transfer.png" style="position: absolute; filter: blur(7px);"/></div>
                <div class="pod-content">
                    <h1>Transfer Your Earnings</h1>
                    <p>With Jules, you have full control over your earnings. Easily transfer the money you make from selling games or in-game items to your bank account. It's your money - you decide what to do with it.</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { gsap } from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';

gsap.registerPlugin(ScrollTrigger);

export default {
    name: 'YourComponentName', // replace with your component name

    mounted() {
        gsap.utils.toArray('.pod, .podr').forEach(pod => {
            const image = pod.querySelector('.circle img');
            const content = pod.querySelector('.pod-content');

            // Animate the image to scale up
            gsap.from(image, {
                scale: 0,
                scrollTrigger: {
                    trigger: pod,
                    start: 'top bottom', // Animation starts when top of element hits bottom of viewport
                    toggleActions: 'play none none none'
                }
            });

            // Animate the text to slide in
            gsap.from(content, {
                x: pod.classList.contains('pod') ? 100 : -100,
                autoAlpha: 0,
                scrollTrigger: {
                    trigger: pod,
                    start: 'top bottom', // Animation starts when top of element hits bottom of viewport
                    toggleActions: 'play none none none'
                }
            });
        });
    }
}
</script>

<style scoped>
.circle {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    background-color: #9E77DA;
    margin-left: 25px;
    margin-right: 25px;
    display: flex;
    justify-content: center;
    align-items: center;

}

.circle img{
    width: 50px;
    height: 50px;
}
.podsTop{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 50px;
}
.podsBottom{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 50px;
}
.podcont{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100vw;
}
.pod{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row-reverse;
    text-align: right;


}

.pod-content{
    color: white;
    width: 390px;
}

.pod-content h1{
    font-size: 14px;
    font-weight: 700;
}
.pod-content p{
    font-size: 12px;
    font-weight: 500;
    color: rgba(255, 255, 255, 0.50);
}
.podr{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    text-align: left;
}

@media only screen and (max-width: 1000px) {
    .pod-content{
    color: white;
    width: 250px;
}

.pod-content h1{
    font-size: 14px;
    font-weight: 700;
}
.pod-content p{
    font-size: 10px;
    font-weight: 500;
    color: rgba(255, 255, 255, 0.50);
}

}

@media only screen and (max-width: 800px) {
    .pod{
        flex-direction: column;
        text-align: center;
        margin-bottom: 25px;
    }
    .podsTop{
        margin-top: 0px;
    }
    .pod-content p{
    font-size: 12px;
    font-weight: 500;
    color: rgba(255, 255, 255, 0.50);
}
    .podr{
        flex-direction: column;
        text-align: center;
    }
    .pod-content{
        width: 80%;
    }
    .podsTop{
        flex-direction: column;
    }
    .podsBottom{
        flex-direction: column;
    }
}
</style>
