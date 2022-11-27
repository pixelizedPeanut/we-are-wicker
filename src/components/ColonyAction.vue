<template>
  <div class="ca">
    <ca-frame>
      <ca-column v-for="(day, index) in days" :day="day.name" :key="index">
        <ca-tile
          v-for="(ca, index) in day.cas"
          :ca="ca.name"
          :reward="ca.reward"
          :tp="ca.tp"
          :bigCa="ca.bigCa"
          :req="ca.req" 
          :key="index"/>
      </ca-column>
    </ca-frame>
  </div>
</template>

<script>
import CaColumn from './CaColumn.vue'
import CaFrame from './CaFrame.vue'
import CaTile from './CaTile.vue'

export default {
  name: 'ColonyAction',
  components: {
    CaColumn,
    CaFrame,
    CaTile
  },
  data() {
    return {
      days: [
        {
          name: "Monday",
          cas: [
            {
              ca: "ca name",
              reward: "speedups",
              tp: "yes",
              bigCa: "no",
              req: "do stuff"
            },
            {
              ca: "ca name2",
              reward: "speedups",
              tp: "yes",
              bigCa: "yes",
              req: "do stuff"
            }
          ]
        },
        {
          name: "Tuesday",
          cas: [
            {
              ca: "ca name",
              reward: "speedups",
              tp: "yes",
              bigCa: "no",
              req: "do stuff"
            },
            {
              ca: "ca name2",
              reward: "speedups",
              tp: "yes",
              bigCa: "yes",
              req: "do stuff"
            }
          ]
        }
      ]
    }
  },
  computed: {

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
