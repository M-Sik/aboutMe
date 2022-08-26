<template>
  <v-card
    style="
      background: #FCAF1B;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      margin: 24px 16px;
      padding: 20px 30px;
    "
  >
    <BoldText
      class="black--text text-center"
      text-value="Skills"
      font-size="20"
    />
    <v-row
      class="mt-6"
      justify="space-between"
      no-gutters
    >
      <v-col cols="auto">
        <div class="mb-10">
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img
                style="object-fit: contain; width: 14vw;"
                src="@/assets/images/htmlImg.png"
              >
            </v-col>
          </v-row>

          <BoldText
            style="text-align: center;"
            class="black--text"
            text-value="HTML"
            font-size="16"
          />
        </div>
        <div>
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img
                style="object-fit: contain; width: 14vw;"
                src="@/assets/images/vueImg.png"
              >
            </v-col>
          </v-row>
          <BoldText
            style="text-align: center;"
            class="black--text"
            text-value="VUE"
            font-size="16"
          />
        </div>
      </v-col>
      <v-col cols="auto">
        <div class="mb-10">
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img
                style="object-fit: contain; width: 14vw;"
                src="@/assets/images/jsImg.png"
              >
            </v-col>
          </v-row>
          <BoldText
            style="text-align: center;"
            class="black--text"
            text-value="JS"
            font-size="16"
          />
        </div>
        <div>
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img
                style="object-fit: contain; width: 14vw;"
                src="@/assets/images/vuetifyImg.png"
              >
            </v-col>
          </v-row>
          <BoldText
            style="text-align: center;"
            class="black--text"
            text-value="VUETIFY"
            font-size="16"
          />
        </div>
      </v-col>
      <v-col cols="auto">
        <div class="mb-10">
          <v-row
            no-gutters
            justify="center"
          >
            <v-col cols="auto">
              <img
                style="object-fit: contain; width: 14vw;"
                src="@/assets/images/cssImg.png"
              >
            </v-col>
          </v-row>
          <BoldText
            style="text-align: center;"
            class="black--text"
            text-value="CSS"
            font-size="16"
          />
        </div>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'

export default {
  name: "MSkills",
  components: {
    BoldText,
  }
}
</script>

<style>

</style>
