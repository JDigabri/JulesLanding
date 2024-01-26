<template>
  <div class="cardHolder" id="cardholder">
    <div class="BigCard">
      <!-- Container for angling the images -->
      <div class="bigcard-image"></div>
      <div class="angledContainer" style="left: -50px">
        <div class="BigCard-inner" ref="bigCardInner">
          <!-- Only one set of images is needed as GSAP will handle the looping -->
          <div
            style="background-image: url('../src/assets/Big/apex.jpg')"
            alt="Apex"
            class="bigImg"
          />
          <div
            style="background-image: url('../src/assets/Big/coldwar.jpg')"
            alt="Apex"
            class="bigImg"
          />
          <div
            style="background-image: url('../src/assets/Big/gta.jpg')"
            alt="Apex"
            class="bigImg"
          />
          <div
            style="background-image: url('../src/assets/Big/Stray.jpg')"
            alt="Apex"
            class="bigImg"
          />
        </div>
      </div>
      <div class="angledContainer" style="left: -140px; top: -32px">
        <div class="BigCard-inner" ref="bigCardInnerSecond">
          <div
            style="background-image: url('../src/assets/Big/dis.webp')"
            alt="Apex"
            class="bigImg"
          />
          <div
            style="background-image: url('../src/assets/Big/hitman.jpg')"
            alt="Apex"
            class="bigImg"
          />
          <div
            style="background-image: url('../src/assets/Big/nba.jpg')"
            alt="Apex"
            class="bigImg"
          />
          <div
            style="background-image: url('../src/assets/Big/r6.jpg')"
            alt="Apex"
            class="bigImg"
          />
        </div>
      </div>

      <div class="textHolder" style="padding-bottom: 25px">
        <h1 class="title">Browse Hundreds of Games On Our User Ran Community Market</h1>
        <p class="subtitle">
          Dive into our vast community market where hundreds of games await. From the latest hits to timeless classics, discover your next gaming adventure with Jules.
        </p>
        <a href="https://jules.gg" class="button" >Go To Market --></a>
      </div>
    </div>
    <div class="smallCardHolder">
      <div class="SmallCard">
        <div
          class="textHolder"
          style="position: absolute; width: 600px; height: 390px; padding-bottom: 25px"
        >
          <h1>Global Community</h1>
          <p class="subtitle">
            Join our global community of gamers. Connect, share, and trade with fellow enthusiasts from around the world. With Jules, you're part of a worldwide network of gaming passion
          </p>
          <a href="https://jules.gg" class="button" >Go To Market --></a>
        </div>
        <div class="globe"></div>
        <div class="jelq">
          <div class="globe" style="position: absolute; filter: blur(75px); z-index: -2"></div>
        </div>
      </div>
      <div class="SmallCard">
        <p class="mainText">752 MS</p>
        <p class="mainText" style="filter: blur(8px)">752 MS</p>

        <div class="textHolder" style="padding-bottom: 25px">
          <h1>Goodbye to Long Start-Up Times</h1>
          <p class="subtitle">
            Experience lightning-fast performance with an average start-up time of 752 MS. Jules ensures quick, seamless access to your favorite games, eliminating long start-up times
          </p>
          <a href="https://jules.gg" class="button" >Go To Market --></a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.jelq {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 387.5px;
  width: 600px;
  position: absolute;
  z-index: -1;
  margin-top: -387.5px;
  overflow: hidden;
}
.angledContainer + .angledContainer {
  margin-top: 325px; /* Adjust as needed */
}

.globe {
  background-image: url('../src/assets/globe.png');
  width: 100%;
  height: 387.5px;
  background-repeat: no-repeat;
  background-size: 70% 100%;
  background-position: flex-start;
  border-radius: 10px;
  background-position: right;
  margin-left: auto;
  opacity: 0.5;
}
.cardHolder {
  display: flex;
  width: 100vw;
  justify-content: center;
  align-items: center;
}
.textHolder {
  display: flex;
  flex-direction: column;
  height: 100%;
  justify-content: flex-end;
  color: white;
  padding: 50px;
  font-family: 'Inter', sans-serif;
  font-weight: 200;
  z-index: 2;
}

.textHolder h1 {
  font-family: 'Inter', sans-serif;
  font-weight: 200;
  font-size: 32px;
}
.textHolder p, a {
  font-family: 'Inter', sans-serif;
  font-weight: 200;
  font-size: 12px;
  line-height: 1.5;
  margin-top: 10px;
  margin-bottom: 10px;
  opacity: 0.5;
  text-decoration: none;
  color: white;
}
.textHolder a:hover {
  opacity: 1;
  cursor: pointer;
}

.BigCard {
  overflow: hidden; /* Hide the overflow to create a viewport */
  border-radius: 10px;
  background: #1a1b2c80;
  height: 800px;
  width: 600px;
  margin-top: 75px;
  position: relative; /* Position relative for the inner container */
}

.BigCard-inner {
  display: flex; /* To align images horizontally */
  position: absolute;
  will-change: transform; /* Optimize for animations */
  margin-top: 25px;
}
.BigCard-inner + .BigCard-inner {
  top: auto; /* Remove top alignment for the bottom set */
  bottom: 0; /* Align the bottom set to the bottom */
}
.angledContainer {
  transform: skewX(0); /* Angle the inner container */
  overflow: hidden; /* Ensure angled images don't overflow */
  height: 300px;
  width: 900px;
  transform: rotate(10deg);
  position: absolute;
  margin-top: 50px;
}
.bigImg {
  width: 210px; /* Set a fixed width for each image */
  height: 250px; /* Set a fixed height for each image */
  border-radius: 10px;
  margin-right: 10px;
  transform: rotate(10deg);
  opacity: 0.25;
  background-size: cover; /* Ensure the image covers the div */
  background-position: center; /* Center the image */

  /* 
  
  &:nth-child(1) { transform: translateY(10px); }
  &:nth-child(2) { transform: translateY(20px); }
  &:nth-child(3) { transform: translateY(30px); }
  &:nth-child(4) { transform: translateY(40px); }
  */
}

.smallCardHolder {
  display: flex;
  flex-direction: column;
  margin-top: 100px;
  margin-left: 25px;
}

.SmallCard {
  width: 600px;
  height: 387.5px;
  flex-shrink: 0;
  border-radius: 10px;
  background: #1a1b2c80;
  margin-bottom: 25px;
}

.bigcard-image {
  width: 410px;
  height: 240px;
  background-image: url('../src/assets/Big/r6.jpg');
  background-repeat: no-repeat;
  background-size: 100% 100%;
  background-position: center;
  position: absolute;
  z-index: 1;
  opacity: 1;
  transform: rotate(20deg);

  border-radius: 10px;
  margin-top: 190px;
  margin-left: 90px;
  box-shadow: 0px 10px 25px 0px rgba(0, 0, 0, 1);
}

@keyframes scrollImages {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-100%); /* Move images to the left by the width of one set */
  }
}

.mainText {
  color: #fff;
  font-family: Bebas Neue;
  font-size: 250px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
  width: 600px;
  height: 387.5px;
  justify-content: center;
  align-items: flex-start;
  display: flex;
  position: absolute;
  opacity: 0.3;
}

@media screen and (max-width: 1100px){
  .cardHolder {
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
.smallCardHolder { 
  width: 100vw;
  margin-left: 0px;
  margin-top: 25px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
  .BigCard {
    width: 80%;
    height: 600px;
    margin-top: 25px;

  }

  .angledContainer {
    width: 150%;

  }
  .textHolder {
    padding: 25px;
  }
  .SmallCard {
    width: 80%;
  }
  .bigcard-image {

    margin-top: 10%;
    margin-left: 20%;
  }
  .mainText {
    width: 100vw;
    height: 300px;
    font-size: 150px;
    margin-left: -80px;

  }
  .jelq{
    width: 100vw;
    right: 10%;
    }
    .mainText{
      width: 100%;
      height: 300px;
      font-size: 250px;
    }

  
}

@media screen and (max-width: 755px){
  .mainText {
    width: 100vw;
    height: 300px;
    font-size: 150px;
    margin-left: 0px;

  }
  .BigCard {
    width: 100%;
    height: 400px;
    margin-top: 25px;

  }
  .angledContainer {
    width: 150%;

  }
  .textHolder {
    padding: 25px;
  }
  .SmallCard {
    width: 100%;
  }
  .bigcard-image {
    display: none;
  }
  .jelq{
    width: 100vw;
    right: 0;
    }
  .textHolder{
    width: 100% !important;
  }

}
</style>

<script>
import { gsap } from 'gsap'

export default {
  name: 'GameSlider',
  mounted() {
    this.startAnimation()
  },
  methods: {
    startAnimation() {
      this.animateSection(this.$refs.bigCardInner)
      this.animateSection(this.$refs.bigCardInnerSecond)
    },
    animateSection(section) {
      const images = section.getElementsByClassName('bigImg')
      const singleImageWidth = images[0].offsetWidth + 10
      let totalWidth = images.length * singleImageWidth

      // Clone images for seamless looping
      Array.from(images).forEach((img) => {
        const clone = img.cloneNode()
        section.appendChild(clone)
      })

      // Update total width for cloned images
      totalWidth *= 2

      // GSAP animation for looping
      gsap.to(section, {
        x: -totalWidth / 2,
        ease: 'none',
        duration: 10,
        repeat: -1,
        modifiers: {
          x: gsap.utils.unitize((x) => parseFloat(x) % totalWidth)
        }
      })
    }
  }
}
</script>
