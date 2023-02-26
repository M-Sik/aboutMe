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
          text-value="Waste Community - (주)위드위"
          font-size="24"
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
          class="mt-2"
          text-value="Waste Community 서비스는 폐기물 관련된 정보를 고유하며 이야기를 나눌 수 있는 공간을 제공하는 서비스이며 반응형 웹으로 구현되어있습니다."
          font-size="19"
        />
        <!-- <v-row
          class="mt-4"
          no-gutters
        >
          <v-col
            class="mr-3"
            cols="auto"
          >
            <v-img
              width="160"
              height="56"
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
              width="160"
              height="56"
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
          src="@/assets/images/wasteCommunity.png"
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
              text-value="Waste Community"
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
              text-value="프로젝트 기간"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="신규개발(2022.10 ~ 2022.11) 서비스 운영 대기중"
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
              text-value="담당 업무"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="front-end(반응형웹 신규개발)"
              font-size="20"
            />
            <NomalText
              text-value="- UI 개발 및 데이터 연계"
              font-size="19"
            />
            <NomalText
              text-value="- 외부모듈 연계(카카오 채널)"
              font-size="19"
            />
            <NomalText
              text-value="- REST API를 위한 axios 공동모듈 구현"
              font-size="19"
            />
            <NomalText
              text-value="- Axios Intercopteors를 이용한 Jwt 인증로직 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 프로젝트 소스 형상관리(Git, Github)"
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
              text-value="Vue.js, Scss, Vuetify, Vuex, Git, GitHub"
              font-size="20"
            />
          </v-col>
        </v-row>

        <!-- <v-row
          class="mt-3"
          no-gutters
        >
          <v-col
            style="width: 100px;"
            cols="auto"
            class="pr-5"
          >
            <BoldText
              text-value="고충 사항"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="처음으로 실무에서 프로젝트를 진행해보니 초기 개발 및 운영에 어려움이 있었습니다."
              font-size="20"
            />
            <BoldText
              class="black--text"
              text-value="1. 중복된 코드(style)"
              font-size="20"
            />
            <NomalText
              text-value="개발 초기에는 inline style 방식으로 화면을 구성하였으나 코드 양이 많아질수록 중복되는 스타일이 많아 어려움이 있었습니다. 이를 해결하기 위해 프로젝트에 scss를 도입하였고 자주 쓰이는 스타일을 변수 및 클래스로 지정하여 이를 해결하였습니다."
              font-size="19"
            />
            <BoldText
              class="black--text mt-1"
              text-value="2. 중복된 코드(js)"
              font-size="20"
            />
            <NomalText
              text-value="여러 js 파일에서 같은 동작을 하는 함수들이 많아 소스 수정 시 여러 js 파일을 수정해야 하는 어려움이 있었습니다. 이를 해결하기 위해 2번 이상 사용하는 함수는 모듈로 작성하여 export처리 하였습니다."
              font-size="19"
            />
            <BoldText
              class="black--text mt-1"
              text-value="3. 응집도"
              font-size="20"
            />
            <NomalText
              text-value="서비스 운영 중 소스를 수정해야 할 때 어떤 파일에서 수정을 해야 할지 찾아가며 시간을 소비하였습니다. 이 문제점을 해결하기 위해 서로 관련 있는 소스, 파일들을 모아서 관리하여 문제를 해결하였습니다."
              font-size="19"
            />
            <BoldText
              class="black--text mt-1"
              text-value="4. 협업"
              font-size="20"
            />
            <NomalText
              text-value="프로젝트를 같이 수행하는 인원들이 모두 프로젝트를 해본 경험이 없었습니다. 작업에 대해 문서 작성을 하지도 않았고 구두로 작업을 진행하였으나 업무가 많을 경우 수정, 개선 사항을 잊는 경우도 종종 발생하여 회사에 notion을 도입하여 이 문제점을 해결하였습니다."
              font-size="19"
            />
          </v-col>
        </v-row> -->

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
              text-value="Front-End 1명, Back-End 1명"
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
              text-value="front-end 기준 100%"
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
