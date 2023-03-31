<template>
  <v-card
    class="wrap-project-card"
  >
    <h2>Chium - (주)느루</h2>
    <!-- <v-btn
      class="mt-2"
      style="color: blue;"
      href="/project-chium.pdf"
      download
    >
      👉 프로젝트 상세내용 다운로드 👈
    </v-btn> -->
    <p class="mt-3">
      chium 서비스는 WebView으로 구현 되어 있으며, 폐기물 배출자와 수거업체를 연결해 주는 폐기물 안전처리 서비스 입니다. 배출자와 수거업체간의 입찰 과정을 통하여 폐기물을 처리하며 배출자는 가장 저렴한 가격에 폐기물을 배출할 수 있습니다.
    </p>
    <div class="mt-3">
      <a
        target="blank"
        href="https://chium.co.kr"
      >👉 프로젝트 웹으로 보러가기 👈</a>
    </div>
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
          id="chiumAos"
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
          id="chiumIos"
          target="blank"
          href="https://apps.apple.com/kr/app/%EC%B9%98%EC%9B%80/id1623767946"
          class="d-none"
        />
      </v-col>
    </v-row>
    <div
      v-show="!detailToggle"
      class="wrap-detail-btn"
      @click="chiumDetail"
    >
      <strong>자세히보기</strong>
      <v-icon size="20">
        mdi-chevron-down
      </v-icon>
    </div>
    <div
      v-show="detailToggle"
      class="wrap-detail-btn"
      @click="chiumDetail"
    >
      <strong>자세히보기</strong>
      <v-icon size="20">
        mdi-chevron-up
      </v-icon>
    </div>
    <v-expand-transition>
      <div v-show="detailToggle">
        <hr class="my-3">
        <div>
          <strong class="item-title">프로젝트</strong>
          <br>
          <strong>chium</strong>
        </div>
        <div class="mt-3">
          <strong class="item-title">프로젝트 기간</strong>
          <br>
          <strong>2021. 12 ~ 2022. 10, 신규 개발 및 운영</strong>
        </div>
        <div class="mt-3">
          <strong class="item-title">담당업무</strong>
          <br>
          <strong>Front-End 개발</strong>
        </div>
        <div>
          <p>
            - WebView를 이용한 Aos, Ios 앱 개발
            <br>
            Ios의 경우 앱 종료 시 웹 로컬스토리지가 초기화되는 문제가 발생하여 Native 저장소에 초기화되지 않아야 할 데이터를 저장하여 문제를 해결하였습니다.
          </p>
          <p>- 상태관리 라이브러리인 Vuex를 이용하여 Props 복잡도 개선</p>
          <p>- Jwt 토큰을 이용한 인증 로직 구현</p>
          <p>- 아임포트 모듈을 이용하여 다날 본인인증 서비스 연동</p>
          <p>- 재사용 되는 UI가 있지만 컴포넌트화 되지 않았던 UI들을 컴포넌트로 변경</p>
          <p>- UI 라이브러리를 적절히 활용하여 빠른 UI 개발</p>
          <p>- 운영 중에 발생하는 버그 및 고객 개선사항에 따른 수정</p>
          <p>- 중복되는 Css Class를 줄이기 위해 재사용 가능한 Class 구축</p>
        </div>
        <div class="mt-3">
          <strong class="item-title">사용기술</strong>
          <br>
          <strong>Vue.js, Css, Vuetify, Vuex, Git, GitHub</strong>
        </div>
        <div class="mt-3">
          <strong class="item-title">개발 인원</strong>
          <br>
          <strong>Front-End 2명, Back-End 2명 (참여율 Front-End 기준 70%)</strong>
        </div>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  name: "MChium",
  data: () => ({
    detailToggle: false,
  }),
  methods: {
    chiumDetail() {
      this.detailToggle = !this.detailToggle
    },
    googlePlayBtn() {
      document.getElementById('chiumAos').click()
    },
    appStoreBtn() {
      document.getElementById('chiumIos').click()
    }
  }
}
</script>

<style scoped lang="scss">
.wrap-project-card {
  background: white;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 15px;
  padding: 16px 12px;
  .wrap-detail-btn {
    cursor: pointer;
    display: flex;
    margin-top: 16px;
  }
  .item-title {
    font-size: 3.2rem;
  }
  h2 {
    font-size: 3.2rem;
  }
  p {
    font-size: 2.8rem;
    margin-bottom: 8px;
    color: $grey;
  }
  a, strong {
    font-size: 2.8rem;
  }
}
</style>
