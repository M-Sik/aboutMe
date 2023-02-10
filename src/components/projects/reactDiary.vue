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
          text-value="My Diary - 개인 프로젝트"
          font-size="24"
        />
        <v-btn
          class="mt-2"
          style="color: blue;"
          href="/project-diary.pdf"
          download
        >
          👉 프로젝트 상세내용 다운로드 👈
        </v-btn>
        <div class="mt-4">
          <a
            target="blank"
            href="https://devsik-diary.netlify.app/"
          >👉 홈페이지 보러가기 👈</a>
        </div>
        <NomalText
          class="mt-2"
          text-value="My Diary는 나의 일상을 기록하는 서비스이며 반응형 웹으로 구현되어있습니다."
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
          src="@/assets/images/reactDiary.jpg"
        >
      </v-col>
    </v-row>
    <v-expand-transition>
      <div v-show="detailToggle">
        <v-divider
          style="border: solid 1px #6D6A6A;"
          class="my-3"
        />
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
              class="text-end"
              text-value="프로젝트"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="My Diary"
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
              class="text-end"
              text-value="도메인"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="https://devsik-diary.netlify.app/"
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
              text-value="개발 언어"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="TypeScript, Html, Css"
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
              text-value="React.js, Zustand, Material-UI, Scss, Git, GitHub"
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
              text-value="느낀점"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="처음 사용해본 React.js"
              font-size="20"
            />
            <BoldText
              class="black--text"
              text-value="1. style"
              font-size="20"
            />
            <NomalText
              text-value="React에서는 Css-in-Js방식을 많이 사용하는것 같습니다. Scss를 사용하여 프로젝트를 진행하고 싶어서 서치를 해보니 Vue에서의 scoped와 같이 React에서도 하나의 컴포넌트에 스타일을 부여하는 방법이 있었습니다. module.scss를 사용하는 것입니다. 이를 활용하여 편하게 마크업을 진행할 수 있었습니다."
              font-size="19"
            />
            <BoldText
              class="black--text mt-1"
              text-value="2. script"
              font-size="20"
            />
            <NomalText
              text-value="Vue Option Api를 사용하여 프로젝트를 진행할 때 React 공식문서를 본적이 있었는데 저에게 어렵게 다가왔었습니다. 그 후 Vue Componition Api를 사용하여 프로젝트를 진행하였고, React프로젝트를 작업하다보니 Vue의 Compotion Api와 script 작성 방법이 비슷하여 어렵지 않게 프로젝트를 진행 하였습니다. Vue와 React는 같은 SPA여서 그런지 비슷한점(Life Cycle, State, State감지 등)이 많았고 프레임워크에 국한되지 않고 Js를 더 열심히 공부해야겠다고 느꼈습니다."
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
              text-value="개발 인원"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="1명, 개인프로젝트"
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
              text-value="100%"
              font-size="20"
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
