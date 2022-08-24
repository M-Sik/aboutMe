<template>
  <v-card
    style="
      background: #111110;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      margin: 10vh 10vw;
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
    <Neuru class="mt-10" />
  </v-card>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'
import Chium from '@/components/projects/chium.vue'
import Neuru from '@/components/projects/neuru.vue'

export default {
  name: 'Projects',
  components: {
    // NomalText,
    BoldText,
    Chium,
    Neuru,
  },
}
</script>

<style>

</style>
