<template>
  <v-card
    class="wrap-project-card"
  >
    <h2>My Diary - 개인 프로젝트</h2>
    <p class="mt-3">
      My Diary는 나의 일상을 기록하는 서비스이며 반응형 웹으로 구현되어있습니다.
    </p>
    <div
      class="mt-3"
    >
      <a
        target="blank"
        href="https://devsik-diary.netlify.app/"
      >👉 프로젝트 웹으로 보러가기 👈</a>
    </div>
    <v-btn
      class="mt-2"
      href="/project-diary.pdf"
      download
    >
      👉 프로젝트 상세내용 다운로드 👈
    </v-btn>
    <div
      v-show="!detailToggle"
      class="wrap-detail-btn"
      @click="diaryDetail"
    >
      <strong>자세히보기</strong>
      <v-icon size="20">
        mdi-chevron-down
      </v-icon>
    </div>
    <div
      v-show="detailToggle"
      class="wrap-detail-btn"
      @click="diaryDetail"
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
          <strong>My Diary</strong>
        </div>
        <div class="mt-3">
          <strong class="item-title">담당 업무</strong>
          <br>
          <strong>Front-End 개발</strong>
        </div>
        <div>
          <p>- 함수형 컴포넌트 기반의 반응형 UI 구현</p>
          <p>- 상태관리 라이브러리인 Zustand를 이용하여 Props 복잡도 개선</p>
          <p>- Material UI를 적절히 활용하여 빠른 UI 개발</p>
          <p>- module.scss 를 이용하여 컴포넌트 스타일링, 공통된 스타일 Class는 common.scss에서 관리</p>
        </div>
        <div class="mt-3">
          <strong class="item-title">사용기술</strong>
          <br>
          <strong>React.js, TypeScript, Zustand, Scss, Material UI, Git, GitHub</strong>
        </div>
        <div class="mt-3">
          <strong class="item-title">느낀점</strong>
          <br>
          <strong>처음 사용해본 React.js</strong>
        </div>
        <div>
          <p>Vue만 이용하여 서비스를 구현해보니 React에 대해 궁금하여 공부하고자 작은 프로젝트를 진행하였습니다. 프로젝트를 진행하며 Vue와 비슷하다는 생각이 들었으며, useState, useEffect, useMemo 등등 Hooks에 대해 공부할 수 있었습니다.</p>
        </div>
        <div class="mt-3">
          <strong class="item-title">개발 인원</strong>
          <br>
          <strong>1명, 개인프로젝트</strong>
        </div>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  components: {
  },
  data: () => ({
    detailToggle: false,
  }),
  methods: {
    diaryDetail() {
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
