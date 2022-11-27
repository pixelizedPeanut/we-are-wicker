<template>
  <div class="ca-column">
    <p>{{day}}</p>
    <slot />
  </div>
</template>

<script>
export default {
  name: 'CaColumn',
  props: {
    day: String
  }
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
