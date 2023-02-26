<template>
  <!-- 웹 화면일때 -->
  <v-row
    no-gutters
    style="height: 100vh;"
    justify="center"
    align="center"
  >
    <v-col
      cols="auto"
      class="pr-10"
    >
      <v-img
        style="width: 25vw;"
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
        text-value="프로그래밍이라는 게임을 즐기며"
        font-size="32"
      />
      <BoldText
        text-value="스타트업에서 일하고있는 2년차"
        font-size="32"
      />
      <BoldText
        text-value="✌️Front-End 개발자 김명식 입니다.✌"
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
a:link {
  color: black;
  text-decoration: none;
}
a:visited {
  color: black;
  text-decoration: none;
}
a:hover {
  color: green;
  text-decoration: none;
}
</style>
