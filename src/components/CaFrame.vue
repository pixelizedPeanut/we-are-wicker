<template>
  <div class="ca-frame">
    <div class="ca-frame-wrapper">
      <div class="spacer"/>
      <ul
        class="ca-frame-hour-block"
        v-for="(hourBlock, index) in hours" :key="index">
        <li
          class="ca-frame-hour-item"
          v-for="(hourItem, index2) in hourBlock" :key="index2">
          {{hourItem}}
        </li>
      </ul>
    </div>
    <slot />
  </div>
</template>

<script>
export default {
  name: 'CaFrame',
  data() {
    return {
      hours: [
        [1,2,3,4],
        [5,6,7,8]
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}
li {
  display: inline-block;
  margin: 0 5px;
}

.ca-frame {
  /* width: 100%; */
  overflow-x: scroll;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
}
.spacer {
  box-sizing: border-box;
  display: block;
  height: 50px;
  overflow-y: scroll;
}
.ca-frame-wrapper {
  width: 100px;
  display: flex;
  align-items: stretch;
  flex-direction: column;
}
.ca-frame-hour-block {
  flex: 3;
  box-sizing: border-box;
}
</style>
