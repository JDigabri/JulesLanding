<template>
  <div class="tabHolder">
    <div class="tabs"></div>
    <div class="tabs2"></div>
    <p class="plus">+</p>
    <div class="tabsBG"></div>
  </div>
  <div class="demoMaster">
    <div class="navbar">
      <div class="topBar"></div>
      <div class="circ"></div>
      <div class="circ"></div>
      <div class="hob">
        <div class="circ"></div>
        <p>Owais Hobbi</p>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="16"
          height="16"
          viewBox="0 0 16 16"
          fill="white"
          style="margin-left: 5px"
        >
          <g clip-path="url(#clip0_168_449)">
            <path
              d="M15.898 4.42336C16.0314 4.28524 16.0276 4.06509 15.8894 3.93166C15.7547 3.80152 15.5411 3.80152 15.4063 3.93166L8.00172 11.3356L0.597811 3.93097C0.464379 3.79285 0.244265 3.78903 0.106107 3.92243C-0.0320187 4.05586 -0.0358334 4.27598 0.0975657 4.41414C0.100369 4.41704 0.103206 4.41987 0.106107 4.42268L7.75621 12.0728C7.89199 12.2085 8.1121 12.2085 8.24792 12.0728L15.898 4.42336Z"
              fill="white"
            />
            <path
              d="M0.00390434 4.1771C0.00354576 3.98505 0.158981 3.82909 0.351027 3.82874C0.44361 3.82857 0.532445 3.86535 0.59784 3.9309L8.00175 11.3355L15.4056 3.9309C15.5416 3.79493 15.762 3.79493 15.898 3.9309C16.034 4.06688 16.034 4.28732 15.898 4.42329L8.24791 12.0734C8.11214 12.2091 7.89202 12.2091 7.75621 12.0734L0.106137 4.42329C0.0407095 4.35809 0.00390434 4.26949 0.00390434 4.1771Z"
              fill="white"
            />
          </g>
          <defs>
            <clipPath id="clip0_168_449">
              <rect width="16" height="16" fill="white" transform="matrix(0 1 -1 0 16 0)" />
            </clipPath>
          </defs>
        </svg>
      </div>
    </div>
    <div class="mainGame">
      <div class="selectgame">
        <div class="selectJules">
          <div class="topBarGame">
            <p>Jules</p>

          </div>
          <div class="gamePrev">
                <img src="../assets/Small/stray.png" /><span>Stray</span>
            </div>
            <div class="gamePrev">
                <img src="../assets/Small/gta.png" /><span>Grand Theft Auto</span>
            </div>
            <div class="gamePrev">
                <img src="../assets/Small/nba.png" /><span>NBA 2K23</span>
            </div>
            <div class="gamePrev">
                <img src="../assets/Small/r6.png" /><span>Rainbow Six Siege</span>
            </div>
            <div class="gamePrev">
                <img src="../assets/Small/apex.png" /><span>Apex Legends</span>
            </div>
            <div class="gamePrev">
                <img src="../assets/Small/coldwar.png" /><span>COD: Cold War</span>
            </div>
        </div>
        <div class="selectSteam">
          <div class="topBarGame">
            <p>Steam</p>
          </div>
          <div class="gamePrev">
                <img src="../assets/Small/stray.png" /><span>Stray</span>
            </div>
            <div class="gamePrev">
                <img src="../assets/Small/gta.png" /><span>Grand Theft Auto</span>
            </div>
            <div class="gamePrev">
                <img src="../assets/Small/nba.png" /><span>NBA 2K23</span>
            </div>
            <div class="gamePrev">
                <img src="../assets/Small/r6.png" /><span>Rainbow Six Siege</span>
            </div>
            <div class="gamePrev">
                <img src="../assets/Small/apex.png" /><span>Apex Legends</span>
            </div>

        </div>
      </div>
      <div class="game"></div>
    </div>
  </div>
</template>

<style scoped>
.demoMaster {
  width: 800px;
  height: 750px;
  flex-shrink: 0;
  border-radius: 0px 25px 25px 25px;
  background: #15181e;
  border: 15px solid rgba(255, 255, 255, 0.1);
  margin-top: 280px;
}

.topBar {
  width: 425px;
  height: 48px;
  border-radius: 5px;
  background: rgba(78, 89, 109, 0.1);
}
.circ {
  width: 48px;
  height: 48px;
  flex-shrink: 0;
  background: rgba(78, 89, 109, 0.1);
  border-radius: 50%;
}
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 20px;
  margin-left: 20px;
  margin-right: 20px;
}
.hob {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.hob p {
  font-family: Inter;
  font-size: 16px;
  font-style: normal;
  font-weight: 200;
  line-height: normal;
  color: #fff;
  margin-left: 10px;
}

.tabs {
  width: 188px;
  height: 44px;
  flex-shrink: 0;
  border-radius: 25px 25px 0px 0px;
  background: #15181e;
  position: absolute;
  margin-top: 251px;
  margin-left: 15px;
  z-index: 2;
}
.tabs2 {
  width: 188px;
  height: 44px;
  flex-shrink: 0;
  border-radius: 25px 25px 0px 0px;
  margin-left: 203px;
  background-color: #181c23;
  position: absolute;
  margin-top: 251px;
  z-index: 2;
  transition: all 0.3s ease-in-out;
}

.tabs2:hover {
  cursor: pointer;
  background-color: #15181eec;
}
.plus {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 44px;
  width: 44px;
  flex-shrink: 0;
  border-radius: 25px 25px 0px 0px;
  margin-left: 392px;
  position: absolute;
  margin-top: 251px;
  border-radius: 50%;
  z-index: 2;
  transition: all 0.3s ease-in-out;
  color: white;
  font-size: 20px;
  font-family: Inter, sans-serif;
  font-weight: 200;
  cursor: pointer;
}

.plus:hover {
  background-color: #181c23;
  cursor: pointer;
}
.tabsBG {
  width: 500px;
  height: 54px;
  flex-shrink: 0;
  border-radius: 25px 25px 0px 0px;

  background: #2d3035;
  position: absolute;
  margin-top: 241px;
  margin-left: 0;
  z-index: 1;
}
.tabHolder {
  position: absolute;
  width: 400px;
  margin-left: 220px;
}
.selectJules {
  width: 278px;
  height: 321px;
  flex-shrink: 0;
  border-radius: 10px 10px 25px 25px;
  background: rgba(78, 89, 109, 0.1);
  margin-top: 20px;
  margin-left: 20px;
}
.selectSteam {
  width: 278px;
  height: 270px;
  flex-shrink: 0;
  border-radius: 10px 10px 25px 25px;
  background: rgba(78, 89, 109, 0.1);
  margin-top: 20px;
  margin-left: 20px;
}
.topBarGame {
  width: 100%;
  height: 48px;
  border-radius: 10px;
  background: rgba(78, 89, 109, 0.1);
  display: flex;
  align-items: center;
}
.topBarGame p {

  font-family: Inter;
  font-size: 20px;
  font-style: normal;
  font-weight: 100;
  line-height: normal;
  color: #fff;
  margin-left: 15px;
}

.gamePrev{
    width: 100%;
    height: 43px;

    display: flex;
    justify-content: flex-start;
    align-items: center;
    cursor: pointer;
    transition: all 0.15s ease-in-out;
}

.gamePrev:hover{
    background-color: #181c23;
}
.gamePrev img{
    margin-left: 15px;
}
.gamePrev span{
    margin-left: 15px;
    font-family: Inter;
    font-size: 16px;
    font-style: normal;
    font-weight: 100;
    line-height: normal;
    color: #fff;
}
</style>
