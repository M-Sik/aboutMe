<template>
  <v-app>
    <MainAppBar />
    <v-main
      class="meBackground pa-0"
    >
      <v-row
        :style="`height: 100%; width: ${clientWidth}px; padding-top: 64px;`"
        no-gutters
        justify="center"
      >
        <v-col style="width: 100%">
          <Profile />
        </v-col>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>
import MainAppBar from '@/components/appBar/mainAppBar.vue'
import Profile from '@/components/profile/profile.vue'
// import NomalText from '@/components/text/text.vue'
// import BoldText from '@/components/text/textBold.vue'

export default {
  components: {
    MainAppBar,
    Profile,
    // NomalText,
    // BoldText
  },
  data: () => ({
    clientWidth: 0
  }),
  created() {
    this.clientWidth = document.documentElement.clientWidth
  }
};
</script>

<style>
</style>
