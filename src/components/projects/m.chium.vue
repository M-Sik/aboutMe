<template>
  <v-card
    style="background: white;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      padding: 16px 12px;"
  >
    <BoldText
      class="black--text"
      text-value="Chium"
      font-size="16"
    />
    <NomalText
      class="mt-3"
      text-value="chium 서비스는 WebView으로 구현 되어 있으며, 폐기물 배출자와 수거업체를 연결해 주는 폐기물 안전처리 서비스 입니다. 배출자와 수거업체간의 입찰 과정을 통하여 폐기물을 처리하며 배출자는 가장 저렴한 가격에 폐기물을 배출할 수 있습니다."
      font-size="14"
    />
    <v-row
      class="mt-3"
      no-gutters
    >
      <v-col
        class="mr-2"
        cols="auto"
      >
        <v-img
          width="117"
          height="41"
          src="@/assets/images/googlePlay.png"
          @click="googlePlayBtn"
        />
        <a
          id="googlePlay"
          target="blank"
          href="https://play.google.com/store/apps/details?id=aos.gonsoftware.chium"
          class="d-none"
        />
      </v-col>
      <v-col cols="auto">
        <v-img
          width="117"
          height="41"
          src="@/assets/images/appStore.png"
          @click="appStoreBtn"
        />
        <a
          id="appStore"
          target="blank"
          href="https://apps.apple.com/kr/app/%EC%B9%98%EC%9B%80/id1623767946"
          class="d-none"
        />
      </v-col>
    </v-row>
    <div
      v-show="!detailToggle"
      class="mt-4"
      style="display: flex;"
      @click="chiumDetail"
    >
      <BoldText
        text-value="자세히보기"
        font-size="12"
        style="flex: 0 0 auto;
                width: auto;
                max-width: 100%;"
      />
      <v-icon size="20">
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
        font-size="12"
        style="flex: 0 0 auto;
                width: auto;
                max-width: 100%;"
      />
      <v-icon size="20">
        mdi-chevron-up
      </v-icon>
    </div>
    <v-expand-transition>
      <div v-show="detailToggle">
        <v-divider
          style="border: solid 1px #6D6A6A;"
          class="my-3"
        />
        <BoldText
          text-value="담당업무"
          font-size="16"
        />
        <BoldText
          text-value="front-end(WebView 신규개발 & 운영)"
          font-size="14"
        />
        <div style="font-size: 12px;">
          - SMS 본인인증 서비스 구현 (아임포트, 다날)
          <br>
          - Rest 통신을 위한 axios 공통 모듈 구현
          <br>
          - 로그인 기능 구현
          <br>
          - axios interceptors를 이용하여 토큰 인증 로직 구현
          <br>
          - 카카오 주소검색 api를 통해 주소검색 기능 구현
          <br>
          - 카카오 map api를 통하여 위도 및 경도 추출 기능 구현
          <br>
          - Vuex 공통 모듈 구현
          <br>
          - 파일 업로드 기능 구현
          <br>
          - Tesseract.js 라이브러리를 이용한 orc기능 구현
          <br>
          - Android, Ios와 통신하기 위한 Bridge 구현
          <br>
          - vue-pinch-zoom 라이브러리를 사용하여 이미지 확대기능 구현
          <br>
          - fcm push별 화면이동 로직 구현
          <br>
          - 서비스를 이용하는 클라이언트의 Os판별 및 저장기능 구현
        </div>
        <BoldText
          class="mt-4"
          text-value="개발언어"
          font-size="16"
        />
        <BoldText
          text-value="javaScript, html, css"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="사용기술"
          font-size="16"
        />
        <BoldText
          text-value="Vue.js, Vuetify, Vuex"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="참여율"
          font-size="16"
        />
        <BoldText
          text-value="front-end 기준 70%"
          font-size="14"
        />
        <BoldText
          text-value="1. 계정 관련(로그인, 회원가입)"
          font-size="14"
        />
        <div style="font-size: 12px;">
          - 회원가입 구현
          <br>
          - 로그인 구현
        </div>
        <BoldText
          text-value="2. 서비스 관련"
          font-size="14"
        />
        <div style="font-size: 12px;">
          - 개인배출자 서비스 구현
          <br>
          - 사업자 배출자 서비스 구현
          <br>
          - 마이페이지(개인배출자, 사업자배출자, 수거업체) 구현
        </div>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'
import NomalText from '@/components/text/text.vue'

export default {
  name: "MChium",
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
    },
    googlePlayBtn() {
      document.getElementById('googlePlay').click()
    },
    appStoreBtn() {
      document.getElementById('appStore').click()
    }
  }
}
</script>

<style>

</style>
