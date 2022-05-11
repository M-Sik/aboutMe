<template>
  <v-card
    style="background: white;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      padding: 20px 20px;"
  >
    <v-row
      justify="space-between"
      no-gutters
    >
      <v-col
        style="width: 40vw"
        cols="auto"
      >
        <BoldText
          class="black--text"
          text-value="chium(Play Store 배포 완료)"
          font-size="24"
        />
        <NomalText
          text-value="chium 서비스는 WebView으로 구현 되어 있으며, 폐기물 배출자와 수거업체를 연결해 주는 폐기물 안전처리 서비스 입니다. 배출자와 수거업체간의 입찰 과정을 통하여 폐기물을 처리하며 배출자는 가장 저렴한 가격에 폐기물을 배출할 수 있습니다."
          font-size="19"
        />
        <div
          v-show="!detailToggle"
          class="mt-4"
          style="display: flex;"
          @click="chiumDetail"
        >
          <BoldText
            text-value="자세히보기"
            font-size="22"
            style="flex: 0 0 auto;
                width: auto;
                max-width: 100%;"
          />
          <v-icon size="35">
            mdi-chevron-down
          </v-icon>
        </div>
        <div
          v-show="detailToggle"
          class="mt-4"
          style="display: flex;"
          @click="chiumDetail"
        >
          <BoldText
            text-value="자세히보기"
            font-size="22"
            style="flex: 0 0 auto;
                width: auto;
                max-width: 100%;"
          />
          <v-icon size="35">
            mdi-chevron-up
          </v-icon>
        </div>
      </v-col>
      <v-col cols="auto">
        <img
          height="280"
          width="160"
          src="@/assets/images/chiumImg.png"
        >
      </v-col>
    </v-row>
    <v-expand-transition>
      <div v-show="detailToggle">
        <v-divider
          style="border: solid 1px #6D6A6A;"
          class="my-3"
        />
        <v-row no-gutters>
          <v-col
            style="width: 100px;"
            cols="auto"
            class="pr-5"
          >
            <BoldText
              text-value="담당 업무"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="front-end(WebView 신규개발 & 운영)"
              font-size="20"
            />
            <NomalText
              text-value="- SMS 본인인증 서비스 구현(아임포트, 다날)"
              font-size="19"
            />
            <NomalText
              text-value="- Rest 통신을 위한 axios 공통 모듈 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 로그인 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- axios interceptors를 이용하여 토큰(access, refresh) 인증 로직 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 카카오 주소검색 api를 통해 주소 검색 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 카카오 map api를 통하여 위, 경도 추출 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- Vuex 공통 모듈 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 파일 업로드 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- Tesseract.js 라이브러리를 이용한 이미지 ocr 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- Android, Ios와 통신하기 위한 bridge 구현"
              font-size="19"
            />
            <NomalText
              text-value="- vue-pinch-zoom 라이브러를 사용하여 이미지 확대 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- fcm 푸쉬 메세지 별 프론트 화면이동 및 데이터 처리 로직 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 서비스를 이용하는 클라이언트의 Os 저장 기능 구현"
              font-size="19"
            />
          </v-col>
        </v-row>

        <v-row
          class="mt-3"
          no-gutters
        >
          <v-col
            style="width: 100px;"
            cols="auto"
            class="pr-5"
          >
            <BoldText
              text-value="개발 언어"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="html, js, css"
              font-size="20"
            />
          </v-col>
        </v-row>

        <v-row
          class="mt-3"
          no-gutters
        >
          <v-col
            style="width: 100px;"
            cols="auto"
            class="pr-5"
          >
            <BoldText
              text-value="사용 기술"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="Vue.js, Vuetify, Vuex"
              font-size="20"
            />
          </v-col>
        </v-row>

        <v-row
          class="mt-3"
          no-gutters
        >
          <v-col
            style="width: 100px;"
            cols="auto"
            class="pr-5"
          >
            <BoldText
              style="text-align: end;"
              text-value="참여율 "
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="font-end 기준 70%"
              font-size="20"
            />
            <BoldText
              class="black--text"
              text-value="1. 계정 관련(로그인, 회원가입)"
              font-size="20"
            />
            <NomalText
              text-value="- 회원가입 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 로그인 구현"
              font-size="19"
            />
            <BoldText
              class="black--text"
              text-value="2. 서비스 관련(개인 배출자, 사업자 배출자, 폐기물 수거 업체, 마이페이지)"
              font-size="20"
            />
            <NomalText
              text-value="- 개인 배출자 서비스 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 사업자 배출자 서비스 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 모든 회원유형 마이페이지 서비스 구현"
              font-size="19"
            />
          </v-col>
        </v-row>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'
import NomalText from '@/components/text/text.vue'

export default {
  name: "Chium",
  components: {
    // NomalText,
    BoldText,
    NomalText
  },
  data: () => ({
    detailToggle: false,
  }),
  methods: {
    chiumDetail() {
      this.detailToggle = !this.detailToggle
    }
  }
}
</script>

<style>

</style>
