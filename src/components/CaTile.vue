<template>
  <div class="ca-tile">
    <ul>
      <li>{{ ca }}</li>
      <li>Reward: {{ reward }}</li>
      <li>Has tp: {{ tp }}</li>
      <li>Is big: {{ bigCa }}</li>
      <li>Requirements: {{ req }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'CatTile',
  props: {
    ca: String,
    reward: String,
    tp: String,
    bigCa: String,
    req: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 10px;
}
.ci-tile {
  box-sizing: border-box;
  flex: 3;
  overflow-y: scroll;
}
</style>
