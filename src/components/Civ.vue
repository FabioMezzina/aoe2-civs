<!-- A single card for a civilization -->
<template>
  <div class="civ" @click="$emit('setCiv', name)">
    <h1>{{ name }}</h1>
    <img :src="'assets/images' + imgUrl" alt="img non caricata">
  </div>
</template>

<script>
export default {
  name: "Civ",
  props: ["name", "imgUrl"]
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/civ";
</style>