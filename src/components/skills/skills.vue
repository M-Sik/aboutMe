<template>
  <v-card
    style="
      background: #FCAF1B;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      margin: 100px 220px;
      padding: 50px 300px;
    "
  >
    <v-row
      justify="center"
      style="padding-bottom: 60px;"
      no-gutters
    >
      <v-col cols="auto">
        <BoldText
          class="black--text"
          text-value="Skills"
          font-size="32"
        />
      </v-col>
    </v-row>
    <v-row
      justify="space-between"
      no-gutters
    >
      <v-col cols="auto">
        <div class="mb-10">
          <img
            style="object-fit: contain;"
            width="110"
            height="120"
            src="@/assets/images/htmlImg.png"
          >
          <BoldText
            style="text-align: center;"
            class="black--text"
            text-value="HTML"
            font-size="24"
          />
        </div>
        <div>
          <img
            height="120"
            width="120"
            style="object-fit: contain;"
            src="@/assets/images/vueImg.png"
          >
          <BoldText
            style="text-align: center;"
            class="black--text"
            text-value="VUE"
            font-size="24"
          />
        </div>
      </v-col>
      <v-col cols="auto">
        <div class="mb-10">
          <img
            style="object-fit: contain;"
            width="110"
            height="120"
            src="@/assets/images/jsImg.png"
          >
          <BoldText
            style="text-align: center;"
            class="black--text"
            text-value="JS"
            font-size="24"
          />
        </div>
        <div>
          <img
            style="object-fit: contain;"
            width="110"
            height="120"
            src="@/assets/images/vuetifyImg.png"
          >
          <BoldText
            style="text-align: center;"
            class="black--text"
            text-value="VUETIFY"
            font-size="24"
          />
        </div>
      </v-col>
      <v-col cols="auto">
        <div class="mb-10">
          <img
            style="object-fit: contain;"
            width="110"
            height="120"
            src="@/assets/images/cssImg.png"
          >
          <BoldText
            style="text-align: center;"
            class="black--text"
            text-value="JS"
            font-size="24"
          />
        </div>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'

export default {
  name: 'Skills',
  components: {
    // NomalText,
    BoldText,
  },
}
</script>

<style>

</style>
