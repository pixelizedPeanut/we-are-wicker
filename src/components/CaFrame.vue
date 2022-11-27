<template>
  <div class="ci-frame">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'CaFrame'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
p {
  display: block;
  width: 100px;
  margin: 10px;
}
</style>
