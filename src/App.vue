<template>
  <section class="phone">
    <div class="header">
      <article class="head-wr">
        <div>
          <svg viewBox="0 0 512 512">
            <g transform="translate(0,23)">
              <circle cx="255.001" cy="433.5" r="33" fill="#000" />
              <path
                d="M506.632,154.864C440.902,84.341,351.895,45.501,255.997,45.5C160.107,45.501,71.1,84.341,5.369,154.864c7.53,8.08-7.085,20.736,0.995,28.267c8.081,7.53,20.736,7.086,28.267-0.995C92.711,119.82,171.327,85.501,256.004,85.5c84.67,0.001,163.286,34.32,221.366,96.636c3.939,4.226,9.28,6.364,14.635,6.364c4.883,0,9.778-1.778,13.632-5.369C513.717,175.599,514.163,162.944,506.632,154.864z"
                fill="#000"
              />
              <path
                d="M433.194,237.458c-48.587-48.954-111.516-75.913-177.196-75.911c-65.695,0.001-128.625,26.961-177.197,75.913c-7.78,7.841-7.731,20.504,0.11,28.284c7.841,7.78,20.504,7.731,28.284-0.11c41.005-41.326,93.851-64.086,148.803-64.087c54.938-0.002,107.784,22.759,148.804,64.089c3.91,3.939,9.052,5.911,14.196,5.911c5.092,0,10.188-1.934,14.09-5.805C440.927,257.961,440.975,245.298,433.194,237.458z"
                fill="#000"
              />
              <path
                d="M353.151,320.292c-26.02-25.779-63.317-41.792-97.339-41.792c-0.004,0-0.011,0-0.015,0h-1.441c-0.006,0-0.009,0-0.015,0c-34.023,0-71.323,16.014-97.342,41.792c-7.846,7.774-7.905,20.437-0.131,28.284c3.911,3.947,9.059,5.924,14.208,5.924c5.087,0,10.176-1.929,14.075-5.792c18.523-18.352,45.68-30.208,69.192-30.208c0.003,0,0.007,0,0.01,0h1.447c0.004,0,0.005,0,0.009,0c23.509,0,50.668,11.857,69.189,30.208c7.846,7.773,20.511,7.717,28.284-0.132C361.057,340.73,360.998,328.066,353.151,320.292z"
                fill="#000"
              />
            </g>
          </svg>
        </div>
        <div>
          <svg viewBox="0 0 512 512">
            <g stroke="#000" stroke-width="50">
              <line x1="20" y1="350" x2="20" y2="495" />
              <line x1="140" y1="250" x2="140" y2="495" />
              <line x1="260" y1="150" x2="260" y2="495" />
              <line x1="380" y1="50" x2="380" y2="495" />
            </g>
          </svg>
        </div>
        <div>
          <svg viewBox="0 0 100 60">
            <path
              d="M91.5,39h-0.6v-8c0-2.2-1.8-4-3.9-4H9c-2.2,0-4,1.8-4,4V69c0,2.2,1.8,4,4,4h78c2.2,0,3.9-1.8,3.9-4v-8h0.6c2,0,3.5-1.7,3.5-3.8V42.8C95,40.7,93.4,39,91.5,39z M91,57h-4.1L87,69L9,69l0-38l78,0v12H91L91,57zM64.9,34.5H83v31H64.9H49.1h-2.3H43H28.8H26H13v-31h13h2.8H43h3.9h2.3H64.9z"
              transform="translate(0 -25)"
            />
          </svg>
        </div>
      </article>
    </div>
    <div class="content">
      <article class="main-wr">
        <transition name="slide" mode="out-in" v-on:leave="bounceBall">
          <div key="1" v-if="tab == 1">
            <img
              src="https://vector-illustrations.s3.eu-west-3.amazonaws.com/undraw-1.svg"
              alt="illustration"
            />
          </div>

          <div key="2" v-else-if="tab == 2">
            <img
              src="https://vector-illustrations.s3.eu-west-3.amazonaws.com/undraw-2.svg"
              alt="illustration"
            />
          </div>
          <div key="3" v-else-if="tab == 3">
            <img
              src="https://vector-illustrations.s3.eu-west-3.amazonaws.com/undraw-3.svg"
              alt="illustration"
            />
          </div>
          <div key="4" v-else-if="tab == 4">
            <img
              src="https://vector-illustrations.s3.eu-west-3.amazonaws.com/undraw-4.svg"
              alt="illustration"
            />
          </div>
          <div key="5" v-else>
            <img
              src="https://vector-illustrations.s3.eu-west-3.amazonaws.com/undraw-5.svg"
              alt="illustration"
            />
          </div>
        </transition>
      </article>
    </div>
    <div class="tabs">
      <nav>
        <ul class="tab-nav">
          <li v-bind:style="[tab == 1 ? { opacity: '0' } : { opacity: '1' }]">
            <svg viewBox="0 0 100 100" @click="changeTab(1)">
              <g
                fill="rgba(0,0,0,0.5)"
                stroke="rgba(0,0,0,0.25)"
                stroke-width="5"
              >
                <path
                  d="M37.3,1H7.9C4.1,1,1,4.1,1,7.9v29.4c0,3.8,3.1,6.9,6.9,6.9h29.4c3.8,0,6.9-3.1,6.9-6.9V7.9C44.3,4.1,41.2,1,37.3,1zM39.9,37.4c0,1.4-1.1,2.6-2.6,2.6H7.9c-1.4,0-2.6-1.1-2.6-2.6V7.9c0-1.4,1.1-2.6,2.6-2.6h29.4c1.4,0,2.6,1.1,2.6,2.6V37.4z"
                />
                <path
                  d="M37.3,55.2H7.9c-3.8,0-6.9,3.1-6.9,6.9v29.4c0,3.8,3.1,6.9,6.9,6.9h29.4c3.8,0,6.9-3.1,6.9-6.9V62.2C44.3,58.4,41.2,55.2,37.3,55.2zM39.9,91.6c0,1.4-1.1,2.6-2.6,2.6H7.9c-1.4,0-2.6-1.1-2.6-2.6V62.2c0-1.4,1.1-2.6,2.6-2.6h29.4c1.4,0,2.6,1.1,2.6,2.6V91.6z"
                />
                <path
                  d="M92.1,1H62.6c-3.8,0-6.9,3.1-6.9,6.9v29.4c0,3.8,3.1,6.9,6.9,6.9h29.4c3.8,0,6.9-3.1,6.9-6.9V7.9C99,4.1,95.9,1,92.1,1zM94.6,37.4c0,1.4-1.1,2.6-2.6,2.6H62.6c-1.4,0-2.6-1.1-2.6-2.6V7.9c0-1.4,1.1-2.6,2.6-2.6h29.4c1.4,0,2.6,1.1,2.6,2.6V37.4z"
                />
                <path
                  d="M92.1,55.2H62.6c-3.8,0-6.9,3.1-6.9,6.9v29.4c0,3.8,3.1,6.9,6.9,6.9h29.4c3.8,0,6.9-3.1,6.9-6.9V62.2C99,58.4,95.9,55.2,92.1,55.2zM94.6,91.6c0,1.4-1.1,2.6-2.6,2.6H62.6c-1.4,0-2.6-1.1-2.6-2.6V62.2c0-1.4,1.1-2.6,2.6-2.6h29.4c1.4,0,2.6,1.1,2.6,2.6V91.6z"
                />
              </g>
            </svg>
          </li>
          <li v-bind:style="[tab == 2 ? { opacity: '0' } : { opacity: '1' }]">
            <svg viewBox="0 0 100 100" @click="changeTab(2)">
              <g fill="rgba(0,0,0,0.5)" transform="translate(0 -10)scale(1.15)">
                <path
                  d="M37.693,24.11H89c3.313,0,6-2.685,6-6c0-3.312-2.688-6-6-6H37.693c-3.313,0-6,2.687-6,6C31.693,21.424,34.38,24.11,37.693,24.11z"
                />
                <path
                  d="M89,75.891H37.693c-3.313,0-6,2.687-6,6s2.687,6,6,6H89c3.313,0,6-2.687,6-6C95,78.578,92.313,75.891,89,75.891z"
                />
                <path
                  d="M89,44.001H37.693c-3.313,0-6,2.686-6,6c0,3.312,2.687,6,6,6H89c3.313,0,6-2.688,6-6C95,46.687,92.313,44.001,89,44.001z"
                />
                <circle cx="13.504" cy="18.11" r="8.504" />
                <circle cx="13.504" cy="50.001" r="8.504" />
                <circle cx="13.504" cy="81.89" r="8.504" />
              </g>
            </svg>
          </li>
          <li v-bind:style="[tab == 3 ? { opacity: '0' } : { opacity: '1' }]">
            <svg viewBox="0 0 100 100" @click="changeTab(3)">
              <g fill="rgba(0,0,0,0.5)">
                <path
                  d="M27.9,52.6c1,1,2.4,1.6,3.8,1.6c1.4,0,2.7-0.5,3.8-1.6c2.1-2.1,2.1-5.5,0-7.5L24,33.7h64.9c2.9,0,5.3-2.4,5.3-5.3S91.8,23,88.9,23H24l11.4-11.4c2.1-2.1,2.1-5.5,0-7.5c-2.1-2.1-5.5-2.1-7.5,0L7.3,24.6c-2.1,2.1-2.1,5.5,0,7.5L27.9,52.6z"
                />
                <path
                  d="M72.1,47.4c-2.1-2.1-5.5-2.1-7.5,0c-2.1,2.1-2.1,5.5,0,7.5L76,66.3H11.1c-2.9,0-5.3,2.4-5.3,5.3S8.2,77,11.1,77H76L64.6,88.4c-2.1,2.1-2.1,5.5,0,7.5c1,1,2.4,1.6,3.8,1.6s2.7-0.5,3.8-1.6l20.5-20.5c2.1-2.1,2.1-5.5,0-7.5L72.1,47.4z"
                />
              </g>
            </svg>
          </li>
          <li v-bind:style="[tab == 4 ? { opacity: '0' } : { opacity: '1' }]">
            <svg viewBox="0 0 100 100" @click="changeTab(4)">
              <path
                fill="rgba(0,0,0,0.5)"
                stroke="rgba(0,0,0,0.5)"
                stroke-width="2"
                transform="translate(-17 -40)scale(1.4 1.8)"
                d="M78.219,75.96H21.78c-2.222,0-4.03-1.808-4.03-4.03V42.795c0-2.222,1.808-4.03,4.03-4.03h56.438c2.223,0,4.031,1.808,4.031,4.03V71.93C82.25,74.152,80.441,75.96,78.219,75.96z M21.78,42.266c-0.288,0-0.53,0.243-0.53,0.53V71.93c0,0.287,0.243,0.53,0.53,0.53h56.438c0.288,0,0.531-0.243,0.531-0.53V42.795c0-0.287-0.243-0.53-0.531-0.53H21.78z M75.102,33.153  c0-0.966-0.783-1.75-1.75-1.75H26.648c-0.966,0-1.75,0.784-1.75,1.75s0.784,1.75,1.75,1.75h46.703C74.318,34.903,75.102,34.119,75.102,33.153zM69.394,25.791c0-0.966-0.783-1.75-1.75-1.75H32.356c-0.966,0-1.75,0.784-1.75,1.75  s0.784,1.75,1.75,1.75h35.288C68.61,27.541,69.394,26.757,69.394,25.791z"
              />
            </svg>
          </li>
          <li v-bind:style="[tab == 5 ? { opacity: '0' } : { opacity: '1' }]">
            <svg viewBox="0 0 100 100" @click="changeTab(5)">
              <g
                fill="rgba(0,0,0,0.5)"
                stroke="rgba(0,0,0,0.5)"
                stroke-width="5"
                transform="translate(-7 -10)scale(1.18)"
              >
                <path
                  d="M70.5,30.5C70.5,19.1962891,61.3037109,10,50,10s-20.5,9.1962891-20.5,20.5S38.6962891,51,50,51S70.5,41.8037109,70.5,30.5zM31.5,30.5C31.5,20.2988281,39.7988281,12,50,12s18.5,8.2988281,18.5,18.5S60.2011719,49,50,49S31.5,40.7011719,31.5,30.5z"
                />
                <path
                  d="M60.4125977,56.8632812H39.5874023C26.0297852,56.8632812,15,67.8935547,15,81.4511719C15,86.1650391,18.8349609,90,23.5488281,90h52.9023438C81.1650391,90,85,86.1650391,85,81.4511719C85,67.8935547,73.9702148,56.8632812,60.4125977,56.8632812zM76.4511719,88H23.5488281C19.9379883,88,17,85.0625,17,81.4511719c0-12.4550781,10.1328125-22.5878906,22.5874023-22.5878906h20.8251953C72.8671875,58.8632812,83,68.9960938,83,81.4511719C83,85.0625,80.0620117,88,76.4511719,88z"
                />
              </g>
            </svg>
          </li>
        </ul>
      </nav>
      <div
        class="tab-ctr"
        v-bind:style="[
          tab == 1
            ? { left: '1%' }
            : tab == 2
            ? { left: '19.5%' }
            : tab == 3
            ? { left: '38%' }
            : tab == 4
            ? { left: '56.5%' }
            : tab == 5
            ? { left: '75%' }
            : null,
        ]"
      >
        <svg viewBox="0 0 1100 600">
          <path
            d="M 0 0 C 150 0 150 350 300 450 C 450 550 650 550 800 450 C 950 350 950 0 1100 0 "
            fill="lightgrey"
          />
          <circle id="sphere" cx="550" cy="125" r="300" fill="#f3f8fe" />
        </svg>
      </div>
    </div>
  </section>
</template>

<script>
import { gsap } from "gsap";
export default {
  data() {
    return {
      tab: 1,
    };
  },
  methods: {
    changeTab(num) {
      this.tab = num;
    },
    bounceBall() {
      let tl = gsap.timeline();
      tl.to("#sphere", {
        cy: "625",
        duration: 0.25,
      }).to("#sphere", { cy: "125", duration: 0.25 }, ">0.3");
    },
  },
};
</script>

<style>
*,
::before,
::after {
  box-sizing: border-box;
}
body {
  overflow: hidden;
}
#app {
  display: grid;
  place-items: center;
  width: 100vw;
  height: 100vh;
}
.phone {
  width: 25vw;
  min-width: 225px;
  max-width: 325px;
  height: 50vw;
  min-height: 450px;
  max-height: 650px;
  margin: auto;
  border: 2px solid black;
  border-radius: 30px;
  background: #f3f8fe;
  position: relative;
  display: grid;
  grid-template-columns: 100%;
  grid-template-rows: 10% 80% 10%;
  overflow: hidden;
}
.header {
  grid-column: 1;
  grid-row: 1 / 2;
}
.head-wr {
  display: flex;
  width: 100%;
  height: 100%;
  border-top-left-radius: 30px;
  border-top-right-radius: 30px;
  justify-content: flex-start;
  align-items: flex-start;
  gap: 3%;
  padding-top: 20px;
  padding-left: 8%;
  position: relative;
}
.head-wr > div {
  width: 2.5vw;
  min-width: 15px;
  max-width: 20px;
  height: 2.5vw;
  min-height: 15px;
  max-height: 20px;
}
.head-wr > div:nth-of-type(3) {
  width: 4vw;
  min-width: 30px;
  max-width: 40px;
  height: 2.5vw;
  min-height: 15px;
  max-height: 20px;
  position: absolute;
  right: 8%;
  transform: rotate(180deg);
}
.head-wr > div > svg {
  width: 100%;
  height: 100%;
  overflow: visible;
}
.content {
  grid-column: 1;
  grid-row: 2/3;
}
.main-wr {
  width: 100%;
  height: 100%;
  display: flex;
  overflow: hidden;
  background: lightgrey;
}
.main-wr > div {
  margin: auto;
  width: 80%;
  height: auto;
  position: relative;
}
.slide-enter-from,
.slide-leave-to {
  transform: translate(120%);
}
.slide-enter-active,
.slide-leave-active {
  transition: transform 0.4s ease-out;
}
.main-wr > div > img {
  max-width: 100%;
  height: auto;
}
.tabs {
  grid-column: 1;
  grid-row: 3/4;
  position: relative;
}
nav {
  position: absolute;
  top: -25%;
  width: 100%;
  height: 100%;
}
.tab-nav {
  position: absolute;
  padding: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  list-style-type: none;
  border-bottom-left-radius: 30px;
  border-bottom-right-radius: 30px;
}
.tab-nav > li {
  width: 2.5vw;
  min-width: 20px;
  max-width: 25px;
  height: 2.5vw;
  min-height: 20px;
  max-height: 25px;
  padding: 1%;
  top: 50%;
  transform: translateY(-38%);
  transition: opacity 0.25s ease 0.075s;
}
.tab-nav > li > svg {
  overflow: visible;
  width: 100%;
  height: 100%;
  cursor: pointer;
}
.tab-ctr {
  position: absolute;
  width: 25%;
  height: 100%;
  bottom: 0;
  transition: all 0.8s ease;
}
.tab-ctr > svg {
  width: 100%;
  height: 65%;
  overflow: visible;
}
</style>
