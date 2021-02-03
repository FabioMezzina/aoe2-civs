<template>
  <div id="app">
    <Card
      v-for="(civ, i) in civdb"
      v-bind:key="i"
      :name="civ.name"
      :imgUrl="civ.imgUrl"
    />
  </div>
</template>

<script>
import civdb from "./assets/database/civdb.js";
import Card from "./components/Card.vue";

export default {
  name: "App",
  components: {
    Card
  },
  data() {
    return {
      civdb: civdb,
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
