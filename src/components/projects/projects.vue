<template>
  <v-card
    style="
      background: #111110;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      margin: 0px 220px;
      padding: 50px 100px;
    "
  >
    <v-row
      justify="center"
      style="padding-bottom: 60px;"
      no-gutters
    >
      <v-col cols="auto">
        <BoldText
          class="white--text"
          text-value="Projects"
          font-size="32"
        />
      </v-col>
    </v-row>
    <Chium />
  </v-card>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'
import Chium from '@/components/projects/chium.vue'

export default {
  name: 'Projects',
  components: {
    // NomalText,
    BoldText,
    Chium,
  },
}
</script>

<style>

</style>
