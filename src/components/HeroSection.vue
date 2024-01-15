<template>
    <div class="hero-section">
        <div class="hero-section-img" ref="heroImage">
            <img src="../assets/store.png" alt="logo" class="storeImg">
        </div>
        <div class="shadowCover"></div>
        <img src="../assets/grad.png" class="grad" />
        <div class="hero-section-text">
            <h1 class="hero-section-title" ref="heroTitle">SELL UNPLAYED GAMES</h1>
            <h1 class="hero-section-title" ref="heroTitle" style="position: absolute; top: 0; filter: blur(5px);">SELL UNPLAYED GAMES</h1>

            <p class="hero-section-subtitle" ref="heroSubtitle">Take Control of Your Game Library. Gone are the days of your games collecting
                digital<br> dust. With Jules, you can sell games you no longer play to other players in our
                user-<br>friendly marketplace, freeing up your library and your wallet.</p>
            <button class="hero-section-button" >Shop Now</button>
        </div>
    </div>
</template>

<script>
import { gsap } from 'gsap';

export default {
    name: 'HeroSection', 
    mounted() {
        gsap.from(this.$refs.heroImage, {
            duration: 1.5,
            y: 135,
            opacity: 0,
            ease: "power3.out"
        });

        gsap.from([this.$refs.heroTitle, this.$refs.heroSubtitle], {
            duration: 1,
            delay: 0.5,
            opacity: 0,
            ease: "power3.out",
            stagger: 0.2
        });
    }
}
</script>


<style scoped>
.hero-section {
    height: 955px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: white;
    position: relative;
}

.hero-section-img {
    background: linear-gradient(245deg, #BDCFFC 32.08%, #9E77DA 67.06%);
    padding: 5px;
    border-radius: 25px;
    display: flex;
    justify-content: center;
    align-items: center;

}

.storeImg {
    width: 900px;
    height: 700px;
    border-radius: 22px;

}

.shadowCover {
    position: absolute;
    height: 600px;
    width: 100%;
    background: linear-gradient(180deg, rgba(21, 24, 30, 0.00) 0.2%, #15181E 48.91%);
    opacity: 1;
    bottom: 0;
}

.grad {
    position: absolute;
    width: 2000px;
    bottom: -270px;
    z-index: 2;
}

.hero-section-text {
    position: absolute;
    z-index: 3;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    bottom: 80px;
}

.hero-section-title {
    text-align: center;
    font-family: Inter, sans-serif;
    font-size: 86px;
    font-style: italic;
    font-weight: 700;
    line-height: normal;
    background: linear-gradient(245deg, #BDCFFC 32.08%, #9E77DA 67.06%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.hero-section-subtitle {
    color: rgba(255, 255, 255, 0.50);
    text-align: center;
    font-family: Inter, sans-serif;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
}


.hero-section-button {
    width: 300px;
    height: 44px;
    flex-shrink: 0;
    background: transparent;
    border: 2px solid #BDCFFC; /* Default border color */
    margin-top: 20px;
    position: relative;
    color: white; /* Default text color */
    cursor: pointer;
    font-family: Inter, sans-serif;
    outline: none;
    overflow: hidden;
    transition: all 0.3s ease-in-out;
    border-radius: 5px;
    font-weight: 500;
    font-size: 14px;
}


.hero-section-button::after {
    content: attr(data);
    display: block;
    font-size: 16px;
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    text-align: center;
    line-height: 44px;
    z-index: 1;
    transition: all 0.3s ease-in-out;
    border-radius: 5px;
}

.hero-section-button:hover {
    background: linear-gradient(245deg, #BDCFFC 32.08%, #9E77DA 67.06%);
    border-color: #9E77DA; /* Transition border color */
}

.hero-section-button:hover::after {
    color: white;
    transition: all 0.3s ease-in-out;
    border-radius: 5px;

}


</style>
