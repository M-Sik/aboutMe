<template>
  <v-card
    style="background: white;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      padding: 16px 12px;"
  >
    <BoldText
      class="black--text"
      text-value="Wegnal - (주)위드위"
      font-size="16"
    />
    <!-- <v-btn
      class="mt-2"
      style="color: blue;"
      href="/project-wasteCommunity.pdf"
      download
    >
      👉 프로젝트 상세내용 다운로드 👈
    </v-btn> -->
    <NomalText
      class="mt-3"
      text-value="Wegnal은 폐기물 처리를 위해 폐기물 배출자와 수거∙처리업체를 매칭시켜주는 서비스입니다. 배출자가 폐기물 배출 신청 시 정해진 반경 내의 수거∙처리업체에게 수거를 요청합니다."
      font-size="14"
    />
    <div class="mt-3">
      <a
        target="blank"
        href="https://wegnal.com/"
      >👉 프로젝트 웹으로 보러가기 👈</a>
    </div>
    <!-- <v-row
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
    </v-row> -->
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
          text-value="Wegnal"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="프로젝트 기간"
          font-size="16"
        />
        <BoldText
          text-value="2023. 01 ~ 신규 개발 및 운영대기"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="담당업무"
          font-size="16"
        />
        <BoldText
          text-value="Front-End 개발"
          font-size="14"
        />
        <div style="font-size: 12px;">
          - Vue.js Option API에서 Composition API로 리펙토링 진행
          <br>
          👉 기존에는 option API를 활용하여 작업하였으나 소스 코드가 많아질수록 연관돼있는 코드가 나누어져있어 로직을 추적하기 어려웠습니다. 이를 해결하기 위해 Composition API를 도입하였습니다.
          <br>
          - 번들 사이즈 최적화(1.51MB => 1.44MB), Code Splitting, Web Font(868KB ⇒ 169KB) 등 최적화 작업 수행
          <br>
          <a
            target="blank"
            href="https://sikk.tistory.com/117"
          >👉 번들사이즈, Code Splitting 최적화 참고 블로그 포스팅 보러가기 👈</a>
          <br>
          <a
            target="blank"
            href="https://sikk.tistory.com/120"
          >👉 Web Font 최적화 참고 블로그 포스팅 보러가기 👈</a>
          <br>
          - Jwt 토큰을 이용한 인증 로직 구현
          <br>
          - 카카오맵 API를 이용하여 지도, 위치기반의 데이터를 다루어 지도로 화면에 표현
          <br>
          - 디자이너와 협업하여 재사용 가능한 UI 설계
          <br>
          - 사내 Wegnal 서비스 관리를 위한 어드민 페이지 개발
        </div>
        <BoldText
          class="mt-4"
          text-value="사용기술"
          font-size="16"
        />
        <BoldText
          text-value="Vue.js, TypeScript, Scss, Vuetify, Vuex, Git, GitHub"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="개발 인원"
          font-size="16"
        />
        <BoldText
          text-value="Front-End 1명, Back-End 1명"
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
