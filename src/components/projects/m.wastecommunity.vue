<template>
  <v-card
    style="background: white;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      padding: 16px 12px;"
  >
    <BoldText
      class="black--text"
      text-value="Waste Community - (주)위드위"
      font-size="16"
    />
    <v-btn
      class="mt-2"
      style="color: blue;"
      href="/project-wasteCommunity.pdf"
      download
    >
      👉 프로젝트 상세내용 다운로드 👈
    </v-btn>
    <NomalText
      class="mt-3"
      text-value="Waste Community 서비스는 폐기물 관련된 정보를 고유하며 이야기를 나눌 수 있는 공간을 제공하는 서비스이며 반응형 웹으로 구현되어있습니다."
      font-size="14"
    />
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
          text-value="Waste Community"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="프로젝트 기간"
          font-size="16"
        />
        <BoldText
          text-value="2022. 11 ~ 신규 개발 및 운영"
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
          - UI Waste Community 신규 개발 및 운영
          <br>
          - 번들 사이즈 최적화(802.28KB => 733.58KB), Code Splitting 등 최적화 작업 수행
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
          - TypeScript 도입 ⇒ 이전에 진행한 Chium 프로젝트를 운영하며 다른 사람의 소스를 수정할 때 데이터 및 타입 유추가 힘들었기 때문에 도입
          <br>
          - 스크롤 이벤트에 부하를 줄이기 위해 Throttling 적용
          <br>
          - 재사용 되는 스크립트를 모듈화하여 중복 스크립트를 줄임(휴대 번호 Mask, 날짜 Format, Rest API 등등)
          <br>
          - 디자이너와 협업하여 재사용 가능한 UI를 설계하여 개발 일정 단축
          <br>
          - UI 라이브러리를 적절히 활용하여 빠른 UI 개발
          <br>
          - 반응형 UI 구현
          <br>
          - 운영 중에 발생하는 버그 및 고객 개선사항에 따른 수정
          <br>
          - 사내 Waste Community 서비스 관리를 위한 어드민 페이지 개발
          <br>
          - 가독성과 관리하기 좋은 Css를 위해 Scss 도입
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
