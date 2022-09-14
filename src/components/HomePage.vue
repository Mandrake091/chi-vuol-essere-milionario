<template>
  <div class="top d-flex justify-content-center align-items-center">
    <img class="logo" src="../assets/images/logo.png" alt="" />
  </div>
</template>

<script>
export default {
  name: "HomePage",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.top {
  height: 30vh;
  width: 100vw;
  background-color: rgb(0, 8, 163);
}
.logo {
  height: 80%;
}
</style>
