<template>
  <v-btn
    fab
    :class="{
      topButton: !$vuetify.breakpoint.mobile,
      mobileTopButton: $vuetify.breakpoint.mobile,
    }"
    @click="upScroll"
  >
    <v-icon
      size="35"
      class="white--text"
    >
      mdi-chevron-up
    </v-icon>
  </v-btn>
</template>

<script>
export default {
  name: "ScrollUpBtn",
  methods: {
    upScroll() {
      // window.scrollTo(0, 0, "smooth");
      window.scrollTo({top: 0, left: 0, behavior: 'smooth'})
    }
  }
}
</script>

<style scoped>
.topButton {
  top: 90%;
  left: 90%;
  border-radius: 50%;
  border: white 1px solid;
  position: fixed;
  z-index: 99;
  background: black !important;
}
.mobileTopButton {
  top: 85%;
  left: 80%;
  border-radius: 50%;
  border: white 1px solid;
  position: fixed;
  z-index: 99;
  background: black !important;
}
</style>
