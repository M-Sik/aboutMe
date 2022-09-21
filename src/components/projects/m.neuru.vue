<template>
  <v-card
    style="background: white;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      padding: 16px 12px;"
  >
    <BoldText
      class="black--text"
      text-value="Neuru HomePage"
      font-size="16"
    />
    <NomalText
      class="mt-3"
      text-value="chium 서비스를 운영하고 있는 회사의 홈페이지 입니다. 데이터 연동이 없는 정적인 반응형 웹 페이지로 구현 되어 있습니다."
      font-size="14"
    />
    <div
      style="font-size: 14px;"
      class="mt-3"
    >
      <a
        target="blank"
        href="https://neuru.in/"
      >👉 홈페이지 보러가기 👈</a>
    </div>
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
          text-value="front-end(신규개발 & 운영)"
          font-size="14"
        />
        <div style="font-size: 12px;">
          - 카카오 api를 이용한 카카오 채널 추가 기능 구현
          <br>
          - 모든 페이지 반응형 웹 구현
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
          text-value="Vue.js, Vuetify, Vuex, Git, GitHub"
          font-size="14"
        />
        <BoldText
          class="mt-4"
          text-value="참여율"
          font-size="16"
        />
        <BoldText
          text-value="100%"
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
  name: "MNeuru",
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
  }
}
</script>

<style scoped>
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
