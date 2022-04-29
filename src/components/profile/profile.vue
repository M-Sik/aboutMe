<template>
  <v-row
    no-gutters
    style="padding-top: 170px; padding-bottom: 170px;"
    justify="center"
  >
    <v-col
      cols="auto"
      class="pr-10"
    >
      <v-img
        width="430"
        height="430"
        src="@/assets/images/profileImg.png"
      />
    </v-col>
    <v-col
      align-self="center"
      cols="auto"
    >
      <BoldText
        text-value="안녕하세요☺️"
        font-size="32"
      />
      <BoldText
        text-value="코드 재사용과"
        font-size="32"
      />
      <BoldText
        text-value="새로운 도전을 즐기며 코딩하고 있는"
        font-size="32"
      />
      <BoldText
        text-value="✌️1년차 front-end 개발자 김명식 입니다.✌"
        font-size="32"
      />
    </v-col>
  </v-row>
</template>

<script>
// import NomalText from '@/components/text/text.vue'
import BoldText from '@/components/text/textBold.vue'
export default {
  name: "Profile",
  components: {
    // MainAppBar,
    // NomalText,
    BoldText
  },
}
</script>

<style scoped>

</style>
