<template>
  <div class="header-container">
    <div class="bg">  
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data(){
    return{
     
    }
  },
};
</script>
<style scoped>
.header-container{
  width: 100%;
  height: 7%;
  position: fixed;
  top: 0;
  left: 0;
  background-color: #fff;
  box-shadow:0 5px 10px -5px #706f6f;
  z-index: 99;
  display: flex;
  justify-content: center;
  align-items: center;
}
.bg{
  width: 50%;
  height: 200%;
  background: url('https://raw.githubusercontent.com/whsprite/img/main/logo.59y8qij9t5o0.png') center;
  background-size: contain;
  background-repeat: no-repeat;

}
</style>
