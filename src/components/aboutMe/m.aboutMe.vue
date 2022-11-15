<template>
  <v-card
    style="
      background: #FFFDFD;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      margin: 24px 16px;
      padding: 20px 16px;
    "
  >
    <BoldText
      class="text-center"
      text-value="ABOUT ME"
      font-size="20"
    />
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
        <BoldText
          text-value="이름"
          font-size="14"
        />
        <NomalText
          text-value="김명식"
          font-size="12"
        />
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
        <BoldText
          text-value="연락처"
          font-size="14"
        />
        <NomalText
          text-value="010-5754-7220"
          font-size="12"
        />
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
        <BoldText
          text-value="생년월일"
          font-size="14"
        />
        <NomalText
          text-value="97.01.13"
          font-size="12"
        />
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
        <BoldText
          text-value="자격증"
          font-size="14"
        />
        <NomalText
          text-value="정보처리기사"
          font-size="12"
        />
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
        <BoldText
          text-value="블로그"
          font-size="14"
        />
        <a
          target="blank"
          style="font-size: 12px; color: #413F3F;"
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
          mdi-email-outline
        </v-icon>
      </v-col>
      <v-col cols="auto">
        <BoldText
          text-value="이메일"
          font-size="14"
        />
        <NomalText
          text-value="rlaaudtlr233@gmail.com"
          font-size="12"
        />
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
        <BoldText
          text-value="학력"
          font-size="14"
        />
        <NomalText
          text-value="서원대학교 정보통신공학과 졸업(2021.02)"
          font-size="12"
        />
        <NomalText
          text-value="학점: 3.94/4.5"
          font-size="12"
        />
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
        <BoldText
          text-value="경력"
          font-size="14"
        />
        <NomalText
          text-value="주식회사 느루(2021.09 ~ 2022.10)"
          font-size="12"
        />
        <NomalText
          text-value="주식회사 위드위(2022.11 ~ 재직중)"
          font-size="12"
        />
        <NomalText
          text-value="담당업무: front-end 개발"
          font-size="12"
        />
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'
import NomalText from '@/components/text/text.vue'

export default {
  name: "MAboutMe",
  components: {
    BoldText,
    NomalText,
  }
}
</script>

<style>
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
