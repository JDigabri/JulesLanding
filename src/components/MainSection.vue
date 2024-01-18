<template>
  <div class="master">
    <bigCard />
    <div class="main">
      <div class="main-content">
        <div class="main-content-text">
          <div class="tag" ref="tag"><span>Developers Supported</span></div>
          <h1>Open-Source Front End</h1>
          <p>
            Enjoy a seamless, gamer-first experience. Turn your unplayed games into real money. At
            Jules, we offer the unique opportunity to sell your games and in-game items securely to
            other players. It's time to turn your unplayed games into new opportunities.
          </p>
          <div class="shop" ref="shop">Go To Store</div>
        </div>

        <div class="grid-container">
          <div class="grid-item" ref="gridItem1">
            <h1>Open-Source Front End</h1>
            <p>
              Enjoy a seamless, gamer-first experience. Turn your unplayed games into real money. At
              Jules, we offer the unique opportunity to sell your games and in-game items securely
              to other players. It's time to turn your unplayed games into new opportunities.
            </p>
            <p class="goto" style="font-weight: 200; " ref="goto">
              Watch Beta Demo -->
            </p>
          </div>
          <div class="grid-item" ref="gridItem2">
            <h1>Open-Source Front End</h1>
            <p>
              Enjoy a seamless, gamer-first experience. Turn your unplayed games into real money. At
              Jules, we offer the unique opportunity to sell your games and in-game items securely
              to other players. It's time to turn your unplayed games into new opportunities.
            </p>
            <p class="goto" style="font-weight: 200" ref="goto">Watch Beta Demo --></p>
          </div>
          <div class="grid-item" ref="gridItem3">
            <h1>Open-Source Front End</h1>
            <p>
              Enjoy a seamless, gamer-first experience. Turn your unplayed games into real money. At
              Jules, we offer the unique opportunity to sell your games and in-game items securely
              to other players. It's time to turn your unplayed games into new opportunities.
            </p>
            <p class="goto" style="font-weight: 200" ref="goto">Watch Beta Demo --></p>
          </div>
          <div class="grid-item" ref="gridItem4">
            <h1>Open-Source Front End</h1>
            <p>
              Enjoy a seamless, gamer-first experience. Turn your unplayed games into real money. At
              Jules, we offer the unique opportunity to sell your games and in-game items securely
              to other players. It's time to turn your unplayed games into new opportunities.
            </p>
            <p class="goto" style="font-weight: 200" ref="goto">Watch Beta Demo --></p>
          </div>
        </div>
      </div>
      <DemoView />
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

.grid-item p {
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
}

.shop:hover {
  background: rgba(217, 217, 217, 0.35);
  cursor: pointer;
}

.goto {
  transition: all 0.1s ease-in-out;
  cursor: pointer;
  color: #bdcffc !important;
}

.goto:hover {
  color: #9e77da !important;
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

    // Animate the shop button to fade in from the left

    // Animate the goto link to fade in from the left

    const gridItemRefs = ['gridItem1', 'gridItem2', 'gridItem3', 'gridItem4']

    // Animate each grid item to fade in from the left
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
