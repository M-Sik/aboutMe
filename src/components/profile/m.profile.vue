<template>
  <v-row
    align="center"
    justify="center"
    no-gutters
    style="height: calc(100vh - 63px);"
  >
    <v-col cols="auto">
      <v-row
        justify="center"
        no-gutters
      >
        <v-col cols="auto">
          <v-img
            style="width: 60vw;"
            src="@/assets/images/profileImg.png"
          />
        </v-col>
      </v-row>
      <div class="mt-4">
        <BoldText
          class="text-center"
          text-value="안녕하세요☺️"
          font-size="14"
        />
        <BoldText
          class="text-center"
          text-value="코드 재사용과 새로운 도전을 즐기며"
          font-size="14"
        />
        <BoldText
          class="text-center"
          text-value="14개월동안 코딩하고 있는"
          font-size="14"
        />
        <BoldText
          class="text-center"
          text-value="✌️front-end 개발자 김명식 입니다.✌"
          font-size="14"
        />
      </div>
    </v-col>
  </v-row>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'
export default {
  name: "MProfile",
  components: {
    // MainAppBar,
    // NomalText,
    BoldText
  },
}
</script>

<style>

</style>
