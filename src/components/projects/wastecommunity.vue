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
              text-value="2022. 11 ~ 신규 개발 및 운영"
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
              text-value="Front-End 개발"
              font-size="20"
            />
            <NomalText
              text-value="- Waste Community 신규 개발 및 운영"
              font-size="19"
            />
            <NomalText
              text-value="- 번들 사이즈 최적화(802.28KB => 733.58KB), Code Splitting 등 최적화 작업 수행"
              font-size="19"
            />
            <a
              target="blank"
              href="https://sikk.tistory.com/117"
            >👉 블로그 포스팅 보러가기 👈</a>
            <NomalText
              text-value="- Jwt 토큰을 이용한 인증 로직 구현"
              font-size="19"
            />
            <NomalText
              text-value="- TypeScript 도입 ⇒ 이전에 진행한 Chium 프로젝트를 운영하며 다른 사람의 소스를 수정할 때 데이터 및 타입 유추가 힘들었기 때문에 도입"
              font-size="19"
            />
            <NomalText
              text-value="- 스크롤 이벤트에 부하를 줄이기 위해 Throttling 적용"
              font-size="19"
            />
            <NomalText
              text-value="- 재사용 되는 스크립트를 모듈화하여 중복 스크립트를 줄임(휴대 번호 Mask, 날짜 Format, Rest API 등등)"
              font-size="19"
            />
            <NomalText
              text-value="- 디자이너와 협업하여 재사용 가능한 UI를 설계하여 개발 일정 단축"
              font-size="19"
            />
            <NomalText
              text-value="- UI 라이브러리를 적절히 활용하여 빠른 UI 개발"
              font-size="19"
            />
            <NomalText
              text-value="- 반응형 UI 구현"
              font-size="19"
            />
            <NomalText
              text-value="- 운영 중에 발생하는 버그 및 고객 개선사항에 따른 수정"
              font-size="19"
            />
            <NomalText
              text-value="- 사내 Waste Community 서비스 관리를 위한 어드민 페이지 개발"
              font-size="19"
            />
            <NomalText
              text-value="- 가독성과 관리하기 좋은 Css를 위해 Scss 도입"
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
              text-value="Vue.js, TypeScript, Scss, Vuetify, Vuex, Git, GitHub"
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
              text-value="Front-End 1명, Back-End 1명"
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
