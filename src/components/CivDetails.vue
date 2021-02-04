<!-- The detailed informations for a civilization -->
<template>
  <div>
    La civiltà selezionata è: {{ name }}
  </div>
</template>

<script>
export default {
  name: "CivDetails",
  props: ["name"]
}
</script>

<style>

</style>