<template>
  <div class="master" id="master">
    <bigCard />
    <div class="main">
      <div class="main-content">
        <div class="main-content-text">
          <div class="tag" ref="tag"><span>Developers Supported</span></div>
          <h1>Open-Source Front End</h1>
          <p>
            Experience the cutting-edge with Jules' open-source front end. Our transparent and
            community-driven interface ensures a more reliable, secure, and user-friendly gaming
            experience
          </p>
          <a href="https://jules.gg" class="shop" ref="shop">Go To Store</a>
        </div>
        <div class="inside"></div>

        <div class="grid-container">
          <div class="grid-item" ref="gridItem1">
            <h1>Stripe Integration</h1>
            <p>
              Our open-source front end integrates with Stripe, providing a secure and reliable
              payment system. This ensures every transaction on Jules is safe, smooth, and
              user-friendly, giving you peace of mind when selling or buying games
            </p>
            <a href="https://jules.gg" class="goto" style="font-weight: 200" ref="goto"
              >Check It Out --></a
            >
          </div>
          <div class="grid-item" ref="gridItem2">
            <h1>Digital Rights Management</h1>
            <p>
              Jules features a custom DRM system designed to protect the rights of game developers
              and players alike. Our unique approach to DRM balances security with usability,
              ensuring your games are safeguarded without compromising the gaming experience.
            </p>
            <a href="https://jules.gg" class="goto" style="font-weight: 200" ref="goto"
              >Check It Out --></a
            >
          </div>
          <div class="grid-item" ref="gridItem3">
            <h1>Universal Launcher Compatibility Including Emulators</h1>
            <p>
              Jules simplifies gaming with universal launcher compatibility, including emulators.
              Access all your games, from any launcher, through Jules. No more switching apps – just
              one platform for all your gaming needs
            </p>
            <a href="https://jules.gg" class="goto" style="font-weight: 200" ref="goto"
              >Check It Out --></a
            >
          </div>
          <div class="grid-item" ref="gridItem4">
            <h1>Plug-In Market</h1>
            <p>
              Elevate your gaming with Jules' Plugin Store. Choose from community-crafted plugins
              for interface customization and added features. Transform your launcher to fit your
              style and needs, enhancing your gaming experience with simple, impactful
              modifications, all in a user-friendly environment
            </p>
            <a href="https://jules.gg" class="goto" style="font-weight: 200" ref="goto"
              >Check It Out --></a
            >
          </div>
        </div>
      </div>
      <DemoView ref="demo" class="demo" />
      <div class="demoImg"></div>
    </div>
  </div>
</template>

<style scoped>
.main {
  width: 100vw;
  height: 1100px;
  background: linear-gradient(270deg, #15151e 0%, #1a1b2c 101.03%);
  border: 1px solid transparent;
  border-image: linear-gradient(
      90deg,
      rgba(255, 255, 255, 0) 0%,
      rgba(255, 255, 255, 0.5) 50%,
      rgba(255, 255, 255, 0) 100%
    )
    1;
  margin-top: 250px;
  display: flex;
  justify-content: center;
  z-index: 9;
}
.main-content {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: column;
  width: 620px;
  
}

.master {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100vw;
  overflow-x: hidden !important;
  max-width: 100vw !important;
}

.main-content-text {
  padding-right: 150px;
  padding-top: 150px;
  margin-top: 100px;
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  flex-direction: column;
  width: 100%;
}

.main-content-text h1 {
  font-family: Inter;
  font-size: 36px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  color: #fff;
  margin-top: 25px;
}

.main-content-text p {
  font-family: Inter;
  font-size: 16px;
  font-style: normal;
  font-weight: 200;
  line-height: normal;
  color: rgba(255, 255, 255, 0.5);
  margin-top: 25px;
}

.tag {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 197px;
  height: 32px;
  flex-shrink: 0;
  border-radius: 10px;
  background-origin: border-box;
  background-clip: content-box, border-box;
  border: 2px solid #bdcffc;
  background: linear-gradient(
    270deg,
    rgba(189, 207, 252, 0.4) -5.11%,
    rgba(158, 119, 218, 0.4) 110.88%,
    rgba(0, 0, 0, 0) 111.02%
  );
}

.tag span {
  background: linear-gradient(270deg, #bdcffc -5.11%, #9e77da 110.88%, rgba(0, 0, 0, 0) 111.02%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-family: Inter;
  font-size: 15px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  /* Creates 2 columns */
  grid-template-rows: repeat(2, 1fr);
  /* Creates 2 rows */
  gap: 20px;
  /* Adjust the gap size as needed */
  margin-top: 50px;
  /* Space between the text and grid */
  margin-right: 150px;
  width: 460px;
}

.grid-item {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  height: 200px;
  /* Example height, adjust as needed */
  /* Add any additional styles for your grid items */
}

.grid-item h1 {
  font-family: Inter;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  color: #ffffff;
}

.grid-item p,
a {
  font-family: Inter;
  font-size: 12px;
  font-style: normal;
  font-weight: 200;
  line-height: normal;
  color: rgba(255, 255, 255, 0.5);
  margin-top: 15px;
}

.shop {
  transition: all 0.3s ease-in-out;

  border-radius: 25px;
  border: 2px solid rgba(255, 255, 255, 0.35);
  background: rgba(217, 217, 217, 0);
  width: 104px;
  height: 38px;
  flex-shrink: 0;
  color: #fff;
  text-align: center;
  font-family: Inter;
  font-size: 13px;
  font-style: normal;
  font-weight: 200;
  line-height: normal;
  display: flex;
  justify-content: center;
  margin-top: 20px;
  align-items: center;
  text-decoration: none;
}

.demoImg {
  display: none;
}

.shop:hover {
  background: rgba(217, 217, 217, 0.35);
  cursor: pointer;
}

.goto {
  text-decoration: none;
  transition: all 0.1s ease-in-out;
  cursor: pointer;
  color: #bdcffc !important;
}

.goto:hover {
  color: #9e77da !important;
}

@media screen and (max-width: 1425px) {
  .demoImg {
    display: inline;
    width: 600px;
    height: 650px;
    background-image: url('../assets/lib.png');
    background-size: 100% 100%;
    background-position: center;
    margin-top: 220px;
  }
}

@media screen and (max-width: 1265px) {
  .demoImg {
    display: none;
  }
  .main-content {
    justify-content: center;
    align-items: center;
  }
  .grid-container {
    margin-right: 0px;
  }
  .main-content-text {
    padding-right: 0px;
    width: 460px;
  }
}

@media screen and (max-width: 800px) {
  .main {
    height: 1700px;
  }
  .main-content {
    justify-content: center;
    align-items: center;
    margin-top: 120px;
  }
  .grid-container {
    margin-right: 0px;
  }
  .main-content-text {
    padding-right: 0px;
    width: 460px;
  }
  .inside {
    display: inline;
    width: 580px !important;
    height: 650px !important;
    background-image: url('../assets/lib.png');
    background-size: 100% 100%;
    background-position: center;
  }
}

@media screen and (max-width: 600px) {
  .main {
    height: 1700px;
  }
  .main-content {
    justify-content: center;
    align-items: center;
    margin-top: 120px;
  }
  .grid-container {
    margin-right: 0px;
    width: 80%;
  }
  .main-content-text {
    padding-right: 0px;
    width: 80%;
  }
  .inside {
    display: inline;
    width: 380px !important;
    height: 400px !important;
    background-image: url('../assets/lib.png');
    background-size: 100% 100%;
    background-position: center;
  }
}

@media screen and (max-width: 420px) {
  .inside {
    display: inline;
    width: 90% !important;
    height: 400px !important;
    background-image: url('../assets/lib.png');
    background-size: 100% 100%;
    background-position: center;
  }
  .main-content {
    justify-content: center;
    align-items: center;
    margin-top: 120px;
  }
  .grid-container p {
    font-size: 9px;
  }
  .main-content-text {
    padding-right: 0px;
  }
}
</style>

<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
import bigCard from './BigCard.vue'
import DemoView from './DemoView.vue'

gsap.registerPlugin(ScrollTrigger)

export default {
  name: 'MainSection',
  components: {
    bigCard,
    DemoView
  },
  mounted() {
    // Animate the tag to fade in from the left
    gsap.from(this.$refs.tag, {
      scrollTrigger: {
        trigger: this.$refs.tag,
        start: 'top bottom',
        toggleActions: 'play none none none'
      },
      duration: 1,
      opacity: 0,
      x: -100,
      ease: 'power2.out'
    })

    const gridItemRefs = ['gridItem1', 'gridItem2', 'gridItem3', 'gridItem4']

    gridItemRefs.forEach((ref) => {
      gsap.from(this.$refs[ref], {
        scrollTrigger: {
          trigger: this.$refs[ref],
          start: 'top bottom',
          toggleActions: 'play none none none'
        },
        duration: 1,
        opacity: 0,
        x: -100,
        ease: 'power2.out'
      })
    })
  }
}
</script>
