<!-- The detailed informations for a civilization -->
<template>
  <div>
    La civiltà selezionata è: {{ civ.name }}
    <img :src="`assets/images${civ.imgUrl}`" alt="img non caricata">
  </div>
</template>

<script>
import civdb from "../assets/database/civdb.js";

export default {
  name: "CivDetails",
  props: ["name"],
  data() {
    return {
      civdb: civdb,
      civ: {}
    }
  },
  watch: {
    name: function(value) {
      this.civ = civdb.find(civ => {
        return civ.name === value;
      })
    }
  }
}
</script>

<style>

</style>