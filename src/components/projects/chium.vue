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
          text-value="Chium"
          font-size="24"
        />
        <NomalText
          class="mt-2"
          text-value="* 서비스 기획 단계부터 참여 하였습니다."
          font-size="19"
        />
        <NomalText
          class="mt-2"
          text-value="chium 서비스는 WebView으로 구현 되어 있으며, 폐기물 배출자와 수거업체를 연결해 주는 폐기물 안전처리 서비스 입니다. 배출자와 수거업체간의 입찰 과정을 통하여 폐기물을 처리하며 배출자는 가장 저렴한 가격에 폐기물을 배출할 수 있습니다."
          font-size="19"
        />
        <v-row
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
        </v-row>
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
          src="@/assets/images/chiumImg.png"
        >
      </v-col>
    </v-row>
    <v-expand-transition>
      <div v-show="detailToggle">
        <v-divider
          style="border: solid 1px #6D6A6A;"
          class="my-3"
        />
        <v-row no-gutters>
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
              text-value="front-end(WebView 신규개발 & 운영)"
              font-size="20"
            />
            <NomalText
              text-value="- 화면 개발 및 데이터 연계"
              font-size="19"
            />
            <NomalText
              text-value="- SMS 본인인증 서비스 구현(아임포트, 다날)"
              font-size="19"
            />
            <NomalText
              text-value="- Rest 통신을 위한 axios 공통 모듈 구현"
              font-size="19"
            />
            <NomalText
              text-value="- axios interceptors를 이용하여 토큰(access, refresh) 인증 로직 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 카카오 주소검색 api를 통해 주소 검색 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 카카오 map api를 통하여 위, 경도 추출 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- Tesseract.js 라이브러리를 이용한 이미지 ocr 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- Android, Ios와 통신하기 위한 bridge 구현"
              font-size="19"
            />
            <NomalText
              text-value="- vue-pinch-zoom 라이브러리를 사용하여 이미지 확대 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- fcm 푸쉬 메세지 별 프론트 화면이동 및 데이터 처리 로직 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 서비스를 이용하는 클라이언트의 Os 저장 기능 구현"
              font-size="19"
            />
            <NomalText
              text-value="- JSDoc을 사용하여 주석 처리 작업 주도"
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
              text-value="javaScript, html, css"
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
              text-value="Vue.js, Vuetify, Vuex"
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
              text-value="front-end 기준 70%"
              font-size="20"
            />
            <BoldText
              class="black--text"
              text-value="1. 계정 관련(로그인, 회원가입)"
              font-size="20"
            />
            <NomalText
              text-value="- 회원가입 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 로그인 구현"
              font-size="19"
            />
            <BoldText
              class="black--text"
              text-value="2. 서비스 관련"
              font-size="20"
            />
            <NomalText
              text-value="- 개인 배출자 서비스 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 사업자 배출자 서비스 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 모든 회원유형 마이페이지 서비스 구현"
              font-size="19"
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
  name: "Chium",
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
