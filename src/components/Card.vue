<template>
  <div>
    <h1>{{ name }}</h1>
    <img :src="'assets/images' + imgUrl" alt="img non caricata">
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["name", "imgUrl"]
}
</script>

<style>

</style>