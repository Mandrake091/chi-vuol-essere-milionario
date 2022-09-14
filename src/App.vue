<template>
  <div id="app">
    <HomePage />
    <GameComponent />
  </div>
</template>

<script>
import HomePage from "./components/HomePage.vue";
import GameComponent from "./components/GameComponent.vue";

export default {
  name: "App",
  components: {
    HomePage,
    GameComponent,
  },
};
</script>

<style lang="scss">
@import "./style/generals.scss";
#app {
  -webkit-font-smoothing: antialiased;
  height: 100vh;
  width: 100vw;
  background-color: rgb(0, 3, 57);
}
</style>
