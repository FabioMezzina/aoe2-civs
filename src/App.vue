<template>
  <div id="app" class="flex">

    <CivList @setCiv="civName = $event" />
    <CivDetails :name="civName" />
  </div>
</template>

<script>
import civdb from "./assets/database/civdb.js";
import CivList from "./components/CivList.vue";
import CivDetails from "./components/CivDetails.vue"

export default {
  name: "App",
  components: {
    CivList,
    CivDetails
  },
  data() {
    return {
      civdb: civdb,
      civName: "",
    };
  },
  methods: {

  }
};
</script>

<style lang="scss">
@import "./assets/scss/variables";
@import "./assets/scss/commons";
@import "./assets/scss/utilities";

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
