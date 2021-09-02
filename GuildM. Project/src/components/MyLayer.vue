<template>
  <transition name="fade" v-show="onMask">
    <div class="mask-layer">
      <div>
        <img
          class="img"
          src="https://raw.githubusercontent.com/whsprite/img/main/LOGO.b54ntsyjk4.gif"
          alt=""
        />
        <a href="#top" class="line" @click="handleMask">エントリー</a>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  methods: {
    handleMask() {
      this.onMask = false;
    },
  },
  data() {
    return {
      onMask: true
    };
  },
};
</script>

<style scoped>
.img {
  width: 100%;
}
.fade-leave-to {
  opacity: 0;
}
.fade-leave-active {
  transition: opacity 1s;
}
.mask-layer {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 999;
  height: 100vh;
  background-image: url(https://raw.githubusercontent.com/whsprite/img/main/back.45ocyue96p20.jpg);
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #fff;
}
.line {
  display: inline-block;
  width: 70%;
  background-color: transparent;
  line-height: 60px;
  color: rgb(255, 255, 255);
  font-size: 28px;
  text-decoration: none;
  border-radius: 30px;
  font-weight: bold;
  box-shadow: 0px 2px 7px 0px #7b7b7c;
  transform: translateY(-50%);
  text-shadow: 0 0 10px rgb(255, 255, 255);
  user-select: none;
  -webkit-user-select: none;
  transform: translateY(-100%);
}
.line::after {
  content: "";
  display: block;
  position: absolute;
  width: 100%;
  height: 60px;
  background-image: linear-gradient(
    45deg,
    rgb(218, 59, 250),
    rgb(39, 132, 255)
  );
  transform: translateY(-100%);
  border-radius: 30px;
  filter: blur(10px);
  z-index: -999;
}
</style>