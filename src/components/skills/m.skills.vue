<template>
  <v-card
    class="wrap-card"
  >
    <h2>Skills</h2>
    <v-row
      class="mt-6"
      justify="space-around"
      no-gutters
    >
      <v-col cols="auto">
        <div class="mb-10">
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img src="@/assets/images/htmlImg.png">
            </v-col>
          </v-row>
          <p>HTML</p>
        </div>
        <div class="mb-10">
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img src="@/assets/images/vueImg.png">
            </v-col>
          </v-row>
          <p>VUE</p>
        </div>
      </v-col>
      <v-col cols="auto">
        <div class="mb-10">
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img src="@/assets/images/jsImg.png">
            </v-col>
          </v-row>
          <p>JS</p>
        </div>
        <div>
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img src="@/assets/images/vuetifyImg.png">
            </v-col>
          </v-row>
          <p>VUETIFY</p>
        </div>
      </v-col>
      <v-col cols="auto">
        <div class="mb-10">
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img src="@/assets/images/cssImg.png">
            </v-col>
          </v-row>
          <p>CSS</p>
        </div>
        <div>
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img src="@/assets/images/tsImg.png">
            </v-col>
          </v-row>
          <p>TS</p>
        </div>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  name: "MSkills",
}
</script>

<style scoped lang="scss">
.wrap-card {
  background: $skills-color;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 15px;
  margin: 24px 16px;
  padding: 20px 16px;
  h2 {
    font-size: 4.0rem;
    text-align: center;
  }
  p {
    text-align: center;
    font-size: 3.2rem;
    font-weight: 700;
  }
  img {
    width: 14vw;
  }
}
</style>
