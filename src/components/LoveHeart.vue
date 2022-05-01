<template>
  <div class="container">
    <div class="heart"></div>
  </div>
</template>

<script>
export default {
  name: "LoveHeart.vue",
};
</script>
<style scoped>
.container {
  margin-top: 30px;
}
.heart {
  position: relative;
  width: 160px;
  height: 146px;
  animation: heartbeat 1s infinite;
  margin: 0 auto;
}
.heart:before,
.heart:after {
  position: absolute;
  content: "";
  left: 80px;
  top: 0;
  width: 80px;
  height: 128px;
  background: #ec2b24;
  -moz-border-radius: 80px 80px 0 0;
  border-radius: 80px 80px 0 0;
  -webkit-transform: rotate(-45deg);
  -moz-transform: rotate(-45deg);
  -ms-transform: rotate(-45deg);
  -o-transform: rotate(-45deg);
  transform: rotate(-45deg);
  -webkit-transform-origin: 0 100%;
  -moz-transform-origin: 0 100%;
  -ms-transform-origin: 0 100%;
  -o-transform-origin: 0 100%;
  transform-origin: 0 100%;
}
.heart:after {
  left: 0;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
  transform: rotate(45deg);
  -webkit-transform-origin: 100% 100%;
  -moz-transform-origin: 100% 100%;
  -ms-transform-origin: 100% 100%;
  -o-transform-origin: 100% 100%;
  transform-origin: 100% 100%;
}

@keyframes heartbeat {
  0% {
    transform: scale(0.75);
  }
  20% {
    transform: scale(1);
  }
  40% {
    transform: scale(0.75);
  }
  60% {
    transform: scale(1);
  }
  80% {
    transform: scale(0.75);
  }
  100% {
    transform: scale(0.75);
  }
}
</style>
