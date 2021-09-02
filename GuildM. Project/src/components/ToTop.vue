<template>
<div class="to-top" @click="backtop" :class="flag ? 'active2' : '' ">
<svg t="1630047506808" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="3055" :class="flag ? 'active' : '' "><path d="M830.24 685.76l11.328-11.312a16 16 0 0 0 0-22.64L530.448 340.688a16 16 0 0 0-22.64 0L196.688 651.808a16 16 0 0 0 0 22.64l11.312 11.312a16 16 0 0 0 22.624 0l288.496-288.512L807.632 685.76a16 16 0 0 0 22.624 0z" p-id="3056"></path></svg>
</div>
</template>
<script>
  export default {
    mounted() {
       window.addEventListener("scroll",this.showbtn,true);
    },
    data(){
        return{
           flag: false, 
        }
    },
    methods: {
       showbtn(){
          let that = this;
          let scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
         if(scrollTop > window.innerHeight){
              this.flag = true;
          }
          if(scrollTop <= window.innerHeight){
              this.flag = false;
          }
       },
      backtop(){
          var timer = setInterval(function(){
            let osTop = document.documentElement.scrollTop || document.body.scrollTop;
            let ispeed = Math.floor(-osTop / 5); 
            document.documentElement.scrollTop = document.body.scrollTop = osTop + ispeed;
            this.isTop = true;
            if(osTop === 0){
              clearInterval(timer);
            }
          },10)
      }
    }
  }
</script>
<style scoped>
.to-top{
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    right: 0;
    top: 50%;
    width: 50px;
    height: 50px;
    background-color: transparent;
    transition: all 0.5s ease-out;
    border-radius: 100%;
    margin: 2%;
}
.icon{
    width: 70%;
    fill: transparent;
    transition: all 0.5s ease-out;
}
.active{
    fill: black;
}
.active2{
    fill: black;
    background-color: rgba(70, 68, 68, 0.308);
}
</style>