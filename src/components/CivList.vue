<!-- Container for all the civilization's cards -->
<template>
  <div class="civ-list flex wrap jc-betwwen">
        <Civ
      v-for="(civ, i) in civdb"
      v-bind:key="i"
      :name="civ.name"
      :imgUrl="civ.imgUrl"
      @setCiv="$emit('setCiv', $event)"
    />
  </div>
</template>

<script>
import civdb from "../assets/database/civdb.js";
import Civ from "./Civ.vue";

export default {
  name: "CivList",
  components: {
    Civ
  },
  data() {
    return {
      civdb: civdb
    }
  }
}
</script>

<style lang="scss">
@import "../assets/scss/civlist";
</style>