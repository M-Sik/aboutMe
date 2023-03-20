<template>
  <v-card
    style="background: white;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      padding: 16px 12px;"
  >
    <BoldText
      class="black--text"
      text-value="My Diary - 개인 프로젝트"
      font-size="16"
    />
    <v-btn
      class="mt-2"
      style="color: blue;"
      href="/project-diary.pdf"
      download
    >
      👉 프로젝트 상세내용 다운로드 👈
    </v-btn>
    <NomalText
      class="mt-3"
      text-value="My Diary는 나의 일상을 기록하는 서비스이며 반응형 웹으로 구현되어있습니다."
      font-size="14"
    />
    <div
      class="mt-3"
    >
      <a
        target="blank"
        href="https://devsik-diary.netlify.app/"
      >👉 프로젝트 웹으로 보러가기 👈</a>
    </div>
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
          text-value="My Diary"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="담당 업무"
          font-size="16"
        />
        <BoldText
          text-value="Front-End 개발"
          font-size="14"
        />
        <div style="font-size: 12px;">
          - 함수형 컴포넌트 기반의 반응형 UI 구현
          <br>
          - 상태관리 라이브러리인 Zustand를 이용하여 Props 복잡도 개선
          <br>
          - Material UI를 적절히 활용하여 빠른 UI 개발
          <br>
          - module.scss 를 이용하여 컴포넌트 스타일링, 공통된 스타일 Class는 common.scss에서 관리
        </div>
        <BoldText
          class="mt-4"
          text-value="사용 기술"
          font-size="16"
        />
        <BoldText
          text-value="React.js, TypeScript, Zustand, Scss, Material UI, Git, GitHub"
          font-size="14"
        />

        <BoldText
          class="mt-4"
          text-value="느낀점"
          font-size="16"
        />
        <BoldText
          class="mt-1"
          text-value="처음 사용해본 React.js"
          font-size="14"
        />
        <div style="font-size: 12px;">
          Vue만 이용하여 서비스를 구현해보니 React에 대해 궁금하여 공부하고자 작은 프로젝트를 진행하였습니다. 프로젝트를 진행하며 Vue와 비슷하다는 생각이 들었으며, useState, useEffect, useMemo 등등 Hooks에 대해 공부할 수 있었습니다.
        </div>
        <BoldText
          class="mt-4"
          text-value="개발 인원"
          font-size="16"
        />
        <BoldText
          text-value="1명, 개인프로젝트"
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
