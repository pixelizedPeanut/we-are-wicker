<template>
  <div class="ca-column">
    <p class="ca-column-title">{{day}}</p>
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
.ca-column {
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
.ca-column-title {
  box-sizing: border-box;
  height: 50px;
  flex: 1;
  overflow-y: scroll;
  margin: 0;
  padding: 0;
}
</style>
