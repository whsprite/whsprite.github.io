<template>
  <div>
    <div class="title">{{t}}</div>
    <div class="card-container">
      <p class="sub-title">{{ title }}</p>
      <div class="text-container">{{ text }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
      title:{
          type:String,
          default: ''
      },
      text:{
          type:String,
          default:''
      },
      t:{
          type:String,
          default:''
      }
  },
};
</script>

<style scoped>
.card-container {
  margin: 15% auto;
  padding: 3%;
  width: 85%;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0px 1px 7px 0px #b4b2b2;
  white-space: pre-line;
}
.sub-title {
  text-align: left;
  font-size: 150%;
  font-weight: bold;
}
.text-container {
  text-align: left;
  margin-bottom: 10%;
  padding: 0 2% 0 2%;
  color: #696969;
  font-size: 14px;
  font-weight: bolder;
  line-height: 2.5;
}
.title{
  width: 80%;
  font-size: 350%;
  margin: 0px;
  font-weight: bold;
  color: #a8a8a8;
  font-family: Arial, Helvetica, sans-serif;
  -webkit-box-reflect: below -20% -webkit-gradient(linear, left top, left bottom, from(transparent), to(rgba(250, 250, 250, 0.3)));
  background-image: linear-gradient(to bottom, #fff 0%, #fff 79%, rgb(63, 63, 63) 80%, rgb(63, 63, 63) 100%, #fff 61%, #fff 100%);
}
</style>