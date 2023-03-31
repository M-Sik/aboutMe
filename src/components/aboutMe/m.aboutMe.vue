<template>
  <v-card
    class="wrap-card"
  >
    <h2>ABOUT ME1</h2>
    <v-row
      class="mt-5"
      no-gutters
    >
      <v-col
        class="pr-2"
        cols="auto"
      >
        <v-icon size="30">
          mdi-account-outline
        </v-icon>
      </v-col>
      <v-col cols="auto">
        <h4>이름</h4>
        <p>김명식</p>
      </v-col>
    </v-row>
    <v-row
      class="mt-4"
      no-gutters
    >
      <v-col
        class="pr-2"
        cols="auto"
      >
        <v-icon size="30">
          mdi-phone-outline
        </v-icon>
      </v-col>
      <v-col cols="auto">
        <h4>연락처</h4>
        <p>010-5754-7220</p>
      </v-col>
    </v-row>
    <v-row
      class="mt-4"
      no-gutters
    >
      <v-col
        class="pr-2"
        cols="auto"
      >
        <v-icon size="30">
          mdi-cake-variant-outline
        </v-icon>
      </v-col>
      <v-col cols="auto">
        <h4>생년월일</h4>
        <p>97.01.13</p>
      </v-col>
    </v-row>
    <v-row
      class="mt-4"
      no-gutters
    >
      <v-col
        class="pr-2"
        cols="auto"
      >
        <v-icon size="30">
          mdi-card-account-details-outline
        </v-icon>
      </v-col>
      <v-col cols="auto">
        <h4>자격증</h4>
        <p>정보처리기사</p>
      </v-col>
    </v-row>
    <v-row
      class="mt-4"
      no-gutters
    >
      <v-col
        class="pr-2"
        cols="auto"
      >
        <v-icon size="30">
          mdi-post-outline
        </v-icon>
      </v-col>
      <v-col cols="auto">
        <h4>Blog</h4>
        <a
          target="blank"
          href="https://sikk.tistory.com/"
        >sikk.tistory.com</a>
      </v-col>
    </v-row>
    <v-row
      class="mt-4"
      no-gutters
    >
      <v-col
        class="pr-2"
        cols="auto"
      >
        <v-icon size="30">
          mdi-link-variant
        </v-icon>
      </v-col>
      <v-col cols="auto">
        <h4>GitHub</h4>
        <a
          target="blank"
          href="https://github.com/M-Sik"
        >github.com/M-Sik</a>
      </v-col>
    </v-row>
    <v-row
      class="mt-4"
      no-gutters
    >
      <v-col
        class="pr-2"
        cols="auto"
      >
        <v-icon size="30">
          mdi-email-outline
        </v-icon>
      </v-col>
      <v-col cols="auto">
        <h4>이메일</h4>
        <p>rlaaudtlr233@gmail.com</p>
      </v-col>
    </v-row>
    <v-row
      class="mt-4"
      no-gutters
    >
      <v-col
        class="pr-2"
        cols="auto"
      >
        <v-icon size="30">
          mdi-account-school-outline
        </v-icon>
      </v-col>
      <v-col cols="auto">
        <h4>학력</h4>
        <p>서원대학교 정보통신공학과 졸업(2021.02)</p>
        <p>학점: 3.94/4.5</p>
      </v-col>
    </v-row>
    <v-row
      class="mt-4"
      no-gutters
    >
      <v-col
        class="pr-2"
        cols="auto"
      >
        <v-icon size="30">
          mdi-account-details-outline
        </v-icon>
      </v-col>
      <v-col cols="auto">
        <h4>경력</h4>
        <p>주식회사 위드위(2022.11 ~ 재직중)</p>
        <p>주식회사 느루(2021.09 ~ 2022.10)</p>
        <p>담당업무: Front-End 개발</p>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  name: "MAboutMe",
}
</script>

<style scoped lang="scss">
.wrap-card {
  background: white;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 15px;
  margin: 24px 16px;
  padding: 20px 16px;
  h2 {
    font-size: 4.0rem;
    text-align: center;
  }
  h4 {
    font-size: 2.8rem;
    color: $grey;
  }
  p, a {
    font-size: 2.4rem;
    color: $grey;
  }

}
</style>
