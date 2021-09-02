<template>
  <a href="javascript:;" class="line">無料で参加する</a>
</template>

<style scoped>
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
  text-shadow: 0 0 10px rgb(255, 255, 255);
  user-select: none;
  -webkit-user-select: none;
  transform: translateY(-50%);
}
.line::after {
  content: "";
  display: block;
  position: absolute;
  width: 100%;
  height: 60px;
  background-image: linear-gradient(
    45deg,
    rgb(228, 248, 112),
    rgb(218, 59, 250),
    rgb(39, 132, 255)
  );
  transform: translateY(-100%);
  border-radius: 30px;
  filter: blur(5px);
  z-index: -999;
}
</style>