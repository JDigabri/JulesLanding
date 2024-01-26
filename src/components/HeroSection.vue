<template>
  <div class="hero-section" id="top">
    <div class="hero-section-img" ref="heroImage">
      <div alt="logo" class="storeImg" />
    </div>
    <div class="shadowCover"></div>
    <img src="../assets/grad.png" class="grad" />
    <div class="hero-section-text">
      <h1 class="hero-section-title" ref="heroTitle">SELL UNPLAYED GAMES</h1>
      <h1
        class="hero-section-title"
        ref="heroTitle"
        style="position: absolute; top: 0; filter: blur(5px)"
      >
        SELL UNPLAYED GAMES
      </h1>

      <p class="hero-section-subtitle" ref="heroSubtitle">
        Take Control of Your Game Library. Gone are the days of your games collecting digital<br />
        dust. With Jules, you can sell games you no longer play to other players in our user-<br />friendly
        marketplace, freeing up your library and your wallet.
      </p>
      <a href="https://jules.gg" class="hero-section-button">Shop Now</a>
    </div>
  </div>
</template>

<script>
import { gsap } from 'gsap'

export default {
  name: 'HeroSection',
  mounted() {
    gsap.from(this.$refs.heroImage, {
      duration: 1.5,
      y: 135,
      opacity: 0,
      ease: 'power3.out'
    })

    gsap.from([this.$refs.heroTitle, this.$refs.heroSubtitle], {
      duration: 1,
      delay: 0.5,
      opacity: 0,
      ease: 'power3.out',
      stagger: 0.2
    })
  }
}
</script>

<style scoped>
.hero-section {
  height: 995px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  color: white;
  position: relative;
  overflow-x: hidden !important;
  overflow-y: clip !important;
}

.hero-section-img {
  background: linear-gradient(245deg, #bdcffc 32.08%, #9e77da 67.06%);
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
  background-image: url(../assets/store.png);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.shadowCover {
  position: absolute;
  height: 600px;
  width: 100%;
  background: linear-gradient(180deg, rgba(21, 24, 30, 0) 0.2%, #15181e 48.91%);
  opacity: 1;
  bottom: 0;
}

.grad {
  position: absolute;
  width: 2000px;
  bottom: -50px;
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
  background: linear-gradient(245deg, #bdcffc 32.08%, #9e77da 67.06%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-section-subtitle {
  color: rgba(255, 255, 255, 0.5);
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
  border: 2px solid #bdcffc;
  /* Default border color */
  margin-top: 20px;
  position: relative;
  color: white;
  /* Default text color */
  cursor: pointer;
  font-family: Inter, sans-serif;
  outline: none;
  overflow: hidden;
  transition: all 0.3s ease-in-out;
  border-radius: 5px;
  font-weight: 500;
  font-size: 14px;
  justify-content: center;
  align-items: center;
  display: flex;
  text-decoration: none;
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
  background: linear-gradient(245deg, #bdcffc 32.08%, #9e77da 67.06%);
  border-color: #9e77da;
  /* Transition border color */
}

.hero-section-button:hover::after {
  color: white;
  transition: all 0.3s ease-in-out;
  border-radius: 5px;
}

body {
  overflow-x: hidden !important;
}

@media (max-width: 1050px) {
  .hero-section {
    width: 100vw;
    height: 900px;
  }

  .hero-section-img {
    width: 90%;
    height: 710px;
    padding: 5px;
    border-radius: 25px;
  }

  .storeImg {
    width: 100%;
    height: 700px;
    border-radius: 22px;
  }

  .hero-section-title {
    font-size: 68px;
  }

  .hero-section-subtitle {
    font-size: 14px;
  }

  .hero-section-button {
    width: 200px;
    height: 40px;
    font-size: 12px;
  }
}

@media (max-width: 600px) {
  .hero-section {
    width: 100vw;
    height: 800px;
  }

  .hero-section-img {
    width: 90%;
    height: 610px;
    padding: 5px;
    border-radius: 25px;
  }

  .storeImg {
    width: 100%;
    height: 600px;
    border-radius: 22px;
    background-size: 150% 100%;
    background-position: top;
  }

  .hero-section-title {
    font-size: 42px;
  }

  .hero-section-subtitle {
    font-size: 10px;
  }

  .hero-section-button {
    width: 200px;
    height: 40px;
    font-size: 12px;
  }
  .hero-section-text {
    bottom: 190px;
  }

  .shadowCover {
    bottom: 50px;
  }
}

@media (max-width: 450px) {
  .hero-section {
    width: 100vw;
    height: 100%;
    margin-top: 100px;
  }
  .hero-section-img {
    width: 90%;
    height: 410px;
    padding: 5px;
    border-radius: 25px;
    margin-bottom: 200px;
  }

  .storeImg {
    width: 100%;
    height: 400px;
    border-radius: 22px;
    background-size: 135% 100%;
    background-position: top;
  }
  .hero-section-text {
    bottom: 180px;
  }

  .hero-section-title {
    font-size: 30px;
  }

  .hero-section-subtitle {
    font-size: 8.5px;
  }

  .hero-section-button {
    width: 150px;
    height: 40px;
    font-size: 12px;
  }
  .shadowCover {
    bottom: 0px;
  }
  .grad {
    position: absolute;
    height: 500px;
    bottom: 0px;
    z-index: 2;
  }
}
</style>
