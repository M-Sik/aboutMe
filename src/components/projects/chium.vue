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
          text-value="Chium - (주)느루"
          font-size="24"
        />
        <!-- <v-btn
          class="mt-2"
          style="color: blue;"
          href="/project-chium.pdf"
          download
        >
          👉 프로젝트 상세내용 다운로드 👈
        </v-btn> -->
        <NomalText
          class="mt-2"
          text-value="chium 서비스는 WebView으로 구현 되어 있으며, 폐기물 배출자와 수거업체를 연결해 주는 폐기물 안전처리 서비스 입니다. 배출자와 수거업체간의 입찰 과정을 통하여 폐기물을 처리하며 배출자는 가장 저렴한 가격에 폐기물을 배출할 수 있습니다."
          font-size="19"
        />
        <div class="mt-4">
          <a
            target="blank"
            href="https://chium.co.kr"
          >👉 프로젝트 웹으로 보러가기 👈</a>
        </div>
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
          style="display: flex; cursor: pointer;"
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
          style="display: flex; cursor: pointer;"
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
              text-value="chium"
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
              text-value="2021. 12 ~ 2022. 10, 신규 개발 및 운영"
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
              text-value="Front-End개발"
              font-size="20"
            />
            <NomalText
              text-value="- 상태관리 라이브러리인 Vuex를 이용하여 Props 복잡도 개선"
              font-size="19"
            />
            <NomalText
              text-value="- Jwt 토큰을 이용한 인증 로직 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 아임포트 모듈을 이용하여 다날 본인인증 서비스 연동"
              font-size="19"
            />
            <NomalText
              text-value="- 재사용 되는 UI가 있지만 컴포넌트화 되지 않았던 UI들을 컴포넌트로 변경"
              font-size="19"
            />
            <NomalText
              text-value="- UI 라이브러리를 적절히 활용하여 빠른 UI 개발"
              font-size="19"
            />
            <NomalText
              text-value="- 운영 중에 발생하는 버그 및 고객 개선사항에 따른 수정"
              font-size="19"
            />
            <NomalText
              text-value="- 중복되는 Css Class를 줄이기 위해 재사용 가능한 Class 구축"
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
              text-value="사용 기술"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="Vue.js, Css, Vuetify, Vuex, Git, GitHub"
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
              text-value="개발 인원"
              font-size="20"
            />
          </v-col>
          <v-col>
            <BoldText
              class="black--text"
              text-value="Front-End 2명, Back-End 2명 (참여율 Front-End 기준 70%)"
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
