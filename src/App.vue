<template>
  <div id="app">
    <vue-scroll-snap :fullscreen="true">
      <div class="item" id="one" style="background: #fffef8">
        <div class="gradient-text" style="margin-top: 20vh">
          生日快乐，我的宝贝
        </div>
        <BlinkRose />
        <div class="gradient-text subtitle">一朵小花送给可爱的你</div>
        <div class="instruction">
          请向下滑
          <div>&#8595;</div>
        </div>
      </div>
      <div class="item" id="two">
        <div class="gradient-text" style="font-size: 28px; margin-top: 8vh">
          这是我怦怦跳的心
        </div>
        <LoveHeart />
        <div
          class="gradient-text subtitle"
          style="margin-top: 20px; margin-bottom: 20px"
        >
          心为何怦怦跳？因为这位姑娘
        </div>
        <img src="./assets/profile.jpg" alt="profile" class="profile-avatar" />
        <div class="instruction">
          请向下滑
          <div>&#8595;</div>
        </div>
      </div>
      <div class="item" id="three">
        <YouAre />
      </div>
    </vue-scroll-snap>
  </div>
</template>

<script>
import VueScrollSnap from "vue-scroll-snap";
import LoveHeart from "@/components/LoveHeart";
import BlinkRose from "@/components/BlinkRose";
import YouAre from "@/components/YouAre";

export default {
  name: "App",
  components: { VueScrollSnap, LoveHeart, BlinkRose, YouAre },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.item {
  position: relative;
}

/* Gradient Text*/
.gradient-text {
  font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
  font-size: 36px;
  font-weight: 400;
  letter-spacing: 2px;
  color: #f35626;
  background-image: linear-gradient(92deg, #f35626, #feab3a);
  -webkit-background-clip: text !important;
  -webkit-text-fill-color: transparent !important;
  animation: hue 10s infinite linear !important;
  margin-bottom: 6px;
}

.subtitle {
  font-size: 20px;
  -webkit-background-clip: text !important;
  -webkit-text-fill-color: transparent !important;
  color: #2c3e50;
  animation: hue 3s infinite linear !important;
  background-image: linear-gradient(50deg, #134857, #3b818c);
}

.instruction {
  width: 100vw;
  text-align: center;
  position: absolute;
  bottom: 36px;
}

@keyframes hue {
  from {
    filter: hue-rotate(0deg);
  }
  to {
    filter: hue-rotate(-360deg);
  }
}

.profile-avatar {
  width: 180px;
  height: 180px;
  border-radius: 90px;
}
</style>
