<template>
  <v-card
    class="wrap-card"
  >
    <h2>Projects</h2>
    <Weganl />
    <ReactDiary class="mt-10" />
    <Wastecommunity class="mt-10" />
    <Chium class="mt-10" />
  </v-card>
</template>

<script>
import Chium from '@/components/projects/chium/chium.vue'
import Wastecommunity from '@/components/projects/wasteCommunity/wastecommunity.vue'
import ReactDiary from '@/components/projects/myDiary/reactDiary.vue'
import Weganl from '@/components/projects/wegnal/wegnal.vue'

export default {
  name: 'Projects',
  components: {
    Chium,
    Wastecommunity,
    ReactDiary,
    Weganl,
  },
}
</script>

<style scoped lang="scss">
.wrap-card {
  background: black;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 15px;
  margin: 10vh 10vw;
  padding: 50px 100px;
  h2 {
    font-size: 3.2rem;
    color: white;
    text-align: center;
    padding-bottom: 60px;
  }
}
</style>
