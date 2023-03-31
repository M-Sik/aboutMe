<template>
  <v-card
    class="wrap-card"
  >
    <h2>Skills</h2>
    <v-row
      justify="space-between"
      no-gutters
    >
      <v-col cols="auto">
        <div class="mb-10">
          <img
            width="110"
            height="120"
            src="@/assets/images/htmlImg.png"
          >
          <p>HTML</p>
        </div>
        <div class="mb-10">
          <img
            height="120"
            width="120"
            src="@/assets/images/vueImg.png"
          >
          <p>VUE</p>
        </div>
      </v-col>
      <v-col cols="auto">
        <div class="mb-10">
          <img
            width="110"
            height="120"
            src="@/assets/images/jsImg.png"
          >
          <p>JS</p>
        </div>
        <div>
          <img
            width="110"
            height="120"
            src="@/assets/images/vuetifyImg.png"
          >
          <p>VUETIFY</p>
        </div>
      </v-col>
      <v-col cols="auto">
        <div class="mb-10">
          <img
            width="110"
            height="120"
            src="@/assets/images/cssImg.png"
          >
          <p>CSS</p>
        </div>
        <div>
          <img
            height="120"
            width="120"
            src="@/assets/images/tsImg.png"
          >
          <p>TS</p>
        </div>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  name: 'Skills',
}
</script>

<style scoped lang="scss">
.wrap-card {
  background: $skills-color;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 15px;
  margin: 10vh 10vw;
  padding: 50px 300px;
  h2 {
    font-size: 3.2rem;
    text-align: center;
    padding-bottom: 60px;
  }
  p {
    font-size: 2.4rem;
    text-align: center;
    font-weight: 700;
  }
}
</style>
