<template>
  <div class="mask-layer" v-show="on">
    <div id="google">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfrbq6kDFUPC1NaS_Oc4P09NdmvW9D9GnLOWUQC5TPv9zvXOA/viewform?embedded=true"
        width="100%"
        height="700px"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >Loading…</iframe
      >
    </div>
    <button class="back" @click="handleBack">X</button>
    <hr />
  </div>
</template>

<script>
export default {
  methods: {
    handleBack() {
        this.$emit("close")
    },
  },
};
</script>

<style scoped>
.back {
  padding: 3%;
  color: black;
  font-size: 28px;
  font-weight: bold;
  position: fixed;
  transform: translateY(-100%);
  bottom: 0;
  left: 50;
  transform: translateX(-50%);
  margin-bottom: 10%;
  border: none;
  background-color: transparent;
  z-index: 99;
}
.mask-layer {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 99;
  height: 100vh;
  background-color: #fff;
}
</style>