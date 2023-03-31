<template>
  <v-card
    class="wrap-project-card"
  >
    <h2>Waste Community - (주)위드위</h2>
    <!-- <v-btn
      class="mt-2"
      style="color: blue;"
      href="/project-wasteCommunity.pdf"
      download
    >
      👉 프로젝트 상세내용 다운로드 👈
    </v-btn> -->
    <p class="mt-3">
      Waste Community 서비스는 폐기물 관련된 정보를 고유하며 이야기를 나눌 수 있는 공간을 제공하는 서비스이며 반응형 웹으로 구현되어있습니다.
    </p>
    <div class="mt-3">
      <a
        target="blank"
        href="https://wastecommunity.com/"
      >👉 프로젝트 웹으로 보러가기 👈</a>
    </div>
    <div
      v-show="!detailToggle"
      class="wrap-detail-btn"
      @click="communityDetail"
    >
      <strong>자세히보기</strong>
      <v-icon size="20">
        mdi-chevron-down
      </v-icon>
    </div>
    <div
      v-show="detailToggle"
      class="wrap-detail-btn"
      @click="communityDetail"
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
          <strong>Waste Community</strong>
        </div>
        <div class="mt-3">
          <strong class="item-title">프로젝트 기간</strong>
          <br>
          <strong>2022. 11 ~ 신규 개발 및 운영대기</strong>
        </div>
        <div class="mt-3">
          <strong class="item-title">담당업무</strong>
          <br>
          <strong>Front-End 개발</strong>
        </div>
        <div>
          <p>
            - 번들 사이즈 최적화(802.28KB ⇒ 733.58KB), Code Splitting, Web Font(4.7MB ⇒ 196KB) 등 최적화 작업 수행
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
          </p>
          <p>- Jwt 토큰을 이용한 인증 로직 구현</p>
          <p>- TypeScript 도입 ⇒ 이전에 진행한 Chium 프로젝트를 운영하며 다른 사람의 소스를 수정할 때 데이터 및 타입 유추가 힘들었기 때문에 도입</p>
          <p>- 스크롤 이벤트에 부하를 줄이기 위해 Throttling 적용</p>
          <p>- 재사용 되는 스크립트를 모듈화하여 중복 스크립트를 줄임(휴대 번호 Mask, 날짜 Format, Rest API 등등)</p>
          <p>- 디자이너와 협업하여 재사용 가능한 UI를 설계하여 개발 일정 단축</p>
          <p>- UI 라이브러리를 적절히 활용하여 빠른 UI 개발</p>
          <p>- 반응형 UI 구현</p>
          <p>- 사내 Waste Community 서비스 관리를 위한 어드민 페이지 개발</p>
          <p>- 가독성과 관리하기 좋은 Css를 위해 Scss 도입</p>
        </div>
        <div class="mt-3">
          <strong class="item-title">사용기술</strong>
          <br>
          <strong>Vue.js, TypeScript, Scss, Vuetify, Vuex, Git, GitHub</strong>
        </div>
        <div class="mt-3">
          <strong class="item-title">개발 인원</strong>
          <br>
          <strong>Front-End 1명, Back-End 1명</strong>
        </div>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    detailToggle: false,
  }),
  methods: {
    communityDetail() {
      this.detailToggle = !this.detailToggle
    },
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
