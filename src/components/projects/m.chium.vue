<template>
  <v-card
    style="background: white;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      padding: 16px 12px;"
  >
    <BoldText
      class="black--text"
      text-value="Chium - (주)느루"
      font-size="16"
    />
    <v-btn
      class="mt-2"
      style="color: blue;"
      href="/project-chium.pdf"
      download
    >
      👉 프로젝트 상세내용 다운로드 👈
    </v-btn>
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
      style="display: flex; cursor: pointer;"
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
      style="display: flex; cursor: pointer;"
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
          class="mt-4"
          text-value="프로젝트"
          font-size="16"
        />
        <BoldText
          text-value="chium"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="프로젝트 기간"
          font-size="16"
        />
        <BoldText
          text-value="2021. 12 ~ 2022. 10, 신규 개발 및 운영"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="담당업무"
          font-size="16"
        />
        <BoldText
          text-value="front-end(WebView 신규개발 & 운영)"
          font-size="14"
        />
        <div style="font-size: 12px;">
          - 웹뷰를 이용한 App 개발
          <br>
          - 상태관리 라이브러리인 Vuex를 이용하여 Props 복잡도 개선
          <br>
          - Jwt 토큰을 이용한 인증 로직 구현
          <br>
          - 아임포트 모듈을 이용하여 다날 본인인증 서비스 연동
          <br>
          - 재사용 되는 UI가 있지만 컴포넌트화 되지 않았던 UI들을 컴포넌트로 변경
          <br>
          - UI 라이브러리를 적절히 활용하여 빠른 UI 개발
          <br>
          - 운영 중에 발생하는 버그 및 고객 개선사항에 따른 수정
          <br>
          - 중복되는 Css Class를 줄이기 위해 재사용 가능한 Class 구축
        </div>
        <BoldText
          class="mt-4"
          text-value="사용기술"
          font-size="16"
        />
        <BoldText
          text-value="Vue.js, Css, Vuetify, Vuex, Git, GitHub"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="개발 인원"
          font-size="16"
        />
        <BoldText
          text-value="Front-End 2명, Back-End 2명 (참여율 Front-End 기준 70%)"
          font-size="14"
        />
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
