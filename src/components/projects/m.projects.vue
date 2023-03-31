<template>
  <v-card
    class="wrap-card"
  >
    <h2>Projects</h2>
    <MWegnal class="mt-6" />
    <MReactDiary class="mt-6" />
    <MWasteCommunity class="mt-6" />
    <MChium class="mt-6" />
  </v-card>
</template>

<script>
import MChium from '@/components/projects/chium/m.chium.vue'
import MWasteCommunity from '@/components/projects/wasteCommunity/m.wastecommunity.vue'
import MReactDiary from '@/components/projects/myDiary/m.reactDiary.vue'
import MWegnal from '@/components/projects/wegnal/m.wegnal.vue'

export default {
  name: "MProjects",
  components: {
    MChium,
    MWasteCommunity,
    MReactDiary,
    MWegnal
  }
}
</script>

<style scoped lang="scss">
.wrap-card {
  background: black;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 15px;
  margin: 24px 16px;
  padding: 20px 12px;
  h2 {
    font-size: 4.0rem;
    text-align: center;
    color: white;
  }
}
</style>
