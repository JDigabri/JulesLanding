<template>
  <div class="hero-section">
    <div class="shadowCover"></div>
    <img src="../assets/grad.png" class="grad" />
    <div class="hero-section-text">
      <h1 class="hero-section-title" ref="heroTitle">NOT JUST FOR DESKTOP</h1>
      <h1
        class="hero-section-title"
        ref="heroTitle"
        style="position: absolute; top: 0; filter: blur(5px)"
      >
        NOT JUST FOR DESKTOP
      </h1>

      <p class="hero-section-subtitle" ref="heroSubtitle">
        Take Control of Your Game Library. Gone are the days of your games collecting digital dust.
        With Jules, you can sell games you no longer play to other players in our user-friendly
        marketplace, freeing up your library and your wallet.
      </p>
      <a href="https://jules.gg" class="hero-section-button">Shop Now</a>
    </div>
    <div class="hero-section-img" ref="heroImage1">
      <div class="storeImg"></div>
    </div>
    <div class="hero-section-img fth" ref="heroImage2">
      <div class="storeImg mobBrowse"></div>
    </div>
    <div class="hero-section-img sth" ref="heroImage3">
      <div class="storeImg mobGame"></div>
    </div>
  </div>
</template>

<script>
import { gsap } from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

export default {
  name: 'YourComponentName',
  mounted() {
    const images = [this.$refs.heroImage1, this.$refs.heroImage2, this.$refs.heroImage3]

    images.forEach((section) => {
      gsap.from(section, {
        y: -100, // Starting position - adjust as needed
        opacity: 0,
        duration: 1, // Animation duration
        scrollTrigger: {
          trigger: section,
          start: 'top bottom-=100', // When to start the animation
          end: 'bottom top+=100',
          toggleActions: 'play none none reverse'
        }
      })
    })
  }
}
</script>

<style scoped>
.hero-section {
  height: auto;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  color: white;
  min-height: 955px;

  position: relative;
  overflow-x: hidden !important;
  overflow-y: clip !important;
}

.mobGame {
  background-image: url('../assets/mobgame.png') !important;
}

.mobBrowse {
  background-image: url('../assets/mobBrowse.png') !important;
}
.fth {
  position: absolute;
  top: -140px;
  margin-right: 450px;
  z-index: -2 !important;
}

.sth {
  position: absolute;
  top: -140px;
  margin-left: 450px;
  z-index: -2 !important;
}
.hero-section-img {
  background: linear-gradient(245deg, #bdcffc 32.08%, #9e77da 67.06%);
  padding: 5px;
  border-radius: 25px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 350px;
  z-index: -1;
}

.storeImg {
  width: 350px;
  height: 700px;
  border-radius: 22px;
  background-image: url('../assets/mobstore.png');
  background-repeat: no-repeat;
  background-size: 100%;
}

.shadowCover {
  position: absolute;
  height: 600px;
  width: 100%;
  background: linear-gradient(180deg, rgba(21, 24, 30, 0) 0.2%, #15181e 48.91%);
  opacity: 1;
  top: 80px;
  transform: rotate(180deg);
}

.grad {
  position: absolute;
  width: 2000px;
  bottom: -180px;
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
  top: 80px;
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
  width: 700px;
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
  display: flex;
  justify-content: center;
  align-items: center;
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

@media screen and (max-width: 840px) {
  .storeImg {
    width: 250px;
    height: 700px;
    border-radius: 22px;
    background-image: url('../assets/mobstore.png');
    background-repeat: no-repeat;
    background-size: 100%;
  }
  .hero-section-title {
    font-size: 60px;
  }
  .hero-section-subtitle {
    width: 80%;
  }
}

@media screen and (max-width: 750px) {
  .storeImg {
    width: 170px;
    height: 500px;
    border-radius: 22px;
    background-image: url('../assets/mobstore.png');
    background-repeat: no-repeat;
    background-size: 100%;
  }
  .hero-section-title {
    font-size: 60px;
  }
  .fth {
    position: absolute;
    top: -100px;
    margin-right: 250px;
    z-index: -2 !important;
    margin-top: 300px !important;
  }

  .sth {
    position: absolute;
    top: -100px;
    margin-left: 250px;
    z-index: -2 !important;
    margin-top: 300px !important;
  }
  .hero-section-img {
    margin-top: 50px;
  }
}

@media screen and (max-width: 460px) {
  .hero-section {
    min-height: 750px;
  }
  .storeImg {
    width: 120px;
    height: 300px;
    border-radius: 22px;
    background-image: url('../assets/mobstore.png');
    background-repeat: no-repeat;
    background-size: 100%;
  }
  .hero-section-title {
    font-size: 40px;
  }
  .hero-section-text {
    top: 50px;
  }
  .hero-section-subtitle {
    font-size: 10px;
  }
  .fth {
    position: absolute;
    top: -100px;
    margin-right: 200px;
    z-index: -2 !important;
    margin-top: 350px !important;
  }

  .sth {
    position: absolute;
    top: -100px;
    margin-left: 200px;
    z-index: -2 !important;
    margin-top: 350px !important;
  }
  .hero-section-img {
    margin-top: 150px;
  }
  .shadowCover {
    margin-top: -50px;
  }
  .grad {
    position: absolute;
    height: 500px;
    bottom: 300px;
    z-index: 2;
  }
}
</style>
