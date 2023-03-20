<template>
  <v-card
    style="
      background: #111110;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      margin: 24px 16px;
      padding: 20px 12px;
    "
  >
    <BoldText
      class="white--text text-center"
      text-value="Projects"
      font-size="20"
    />
    <MWegnal class="mt-6" />
    <MReactDiary class="mt-6" />
    <MWasteCommunity class="mt-6" />
    <MChium class="mt-6" />
  </v-card>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'
import MChium from '@/components/projects/m.chium.vue'
import MWasteCommunity from '@/components/projects/m.wastecommunity.vue'
import MReactDiary from '@/components/projects/m.reactDiary.vue'
import MWegnal from '@/components/projects/m.wegnal.vue'

export default {
  name: "MProjects",
  components: {
    BoldText,
    MChium,
    MWasteCommunity,
    MReactDiary,
    MWegnal
  }
}
</script>

<style>

</style>
