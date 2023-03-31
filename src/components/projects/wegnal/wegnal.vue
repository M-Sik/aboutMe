<template>
  <v-card
    class="wrap-project-card"
  >
    <v-row
      justify="space-between"
      no-gutters
    >
      <v-col
        style="width: 40vw"
        cols="auto"
      >
        <h2>Wegnal - (주)위드위</h2>
        <!-- <v-btn
          class="mt-2"
          style="color: blue;"
          href="/project-wasteCommunity.pdf"
          download
        >
          👉 프로젝트 상세내용 다운로드 👈
        </v-btn> -->
        <p class="mt-2">
          Wegnal은 폐기물 처리를 위해 폐기물 배출자와 수거∙처리업체를 매칭시켜주는 서비스입니다. 배출자가 폐기물 배출 신청 시 정해진 반경 내의 수거∙처리업체에게 수거를 요청합니다.
        </p>
        <div class="mt-4">
          <a
            target="blank"
            href="https://wegnal.com/"
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
              id="wegnalAos"
              target="blank"
              href="https://play.google.com/store/apps/details?id=aos.gonsoftware.wegnal"
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
              id="wegnalIos"
              target="blank"
              href="https://apps.apple.com/us/app/%EC%9B%A8%EA%B7%B8%EB%84%90/id6446239095"
              class="d-none"
            />
          </v-col>
        </v-row>
        <div
          v-show="!detailToggle"
          class="wrap-detail-btn"
          @click="wegnalDetail"
        >
          <strong>자세히보기</strong>
          <v-icon size="30">
            mdi-chevron-down
          </v-icon>
        </div>
        <div
          v-show="detailToggle"
          class="wrap-detail-btn"
          @click="wegnalDetail"
        >
          <strong>자세히보기</strong>
          <v-icon size="30">
            mdi-chevron-up
          </v-icon>
        </div>
      </v-col>
      <v-col cols="auto">
        <img
          height="280"
          width="160"
          src="@/assets/images/wegnal.jpg"
        >
      </v-col>
    </v-row>
    <v-expand-transition>
      <div v-show="detailToggle">
        <hr class="my-3">
        <v-row
          class="mt-3"
          no-gutters
        >
          <v-col
            cols="auto"
            class="item-type"
          >
            <strong>프로젝트</strong>
          </v-col>
          <v-col>
            <strong class="black--text">Wegnal</strong>
          </v-col>
        </v-row>
        <v-row
          class="mt-3"
          no-gutters
        >
          <v-col
            cols="auto"
            class="item-type"
          >
            <strong>프로젝트 기간</strong>
          </v-col>
          <v-col>
            <strong class="black--text">2023. 01 ~ 신규 개발 및 운영대기</strong>
          </v-col>
        </v-row>
        <v-row
          class="mt-3"
          no-gutters
        >
          <v-col
            cols="auto"
            class="item-type"
          >
            <strong>담당 업무</strong>
          </v-col>
          <v-col>
            <strong class="black--text">Front-End 개발</strong>
            <p>
              - WebView를 이용한 Aos, Ios 앱 개발
              <br>
              Ios의 경우 앱 종료 시 웹 로컬스토리지가 초기화되는 문제가 발생하여 Native 저장소에 초기화되지 않아야 할 데이터를 저장하여 문제를 해결하였습니다.
            </p>
            <p>
              - Vue.js Option API에서 Composition API로 리펙토링 진행
              <br>
              기존에는 option API를 활용하여 작업하였으나 소스 코드가 많아질수록 연관돼있는 코드가 나누어져있어 로직을 추적하기 어려웠습니다. 이를 해결하기 위해 Composition API를 도입하였습니다.
            </p>
            <p>
              - 번들 사이즈 최적화(1.51MB => 1.44MB), Code Splitting, Web Font(868KB ⇒ 169KB) 등 최적화 작업 수행
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
            <p>- 카카오맵 API를 이용하여 지도, 위치기반의 데이터를 다루어 지도로 화면에 표현</p>
            <p>- 디자이너와 협업하여 재사용 가능한 UI 설계</p>
            <p>- 사내 Wegnal 서비스 관리를 위한 어드민 페이지 개발</p>
          </v-col>
        </v-row>

        <v-row
          class="mt-3"
          no-gutters
        >
          <v-col
            cols="auto"
            class="item-type"
          >
            <strong>사용 기술</strong>
          </v-col>
          <v-col>
            <strong class="black--text">Vue.js, TypeScript, Scss, Vuetify, Vuex, Git, GitHub</strong>
          </v-col>
        </v-row>

        <v-row
          class="mt-3"
          no-gutters
        >
          <v-col
            cols="auto"
            class="item-type"
          >
            <strong>개발 인원</strong>
          </v-col>
          <v-col>
            <strong class="black--text">Front-End 1명, Back-End 1명</strong>
          </v-col>
        </v-row>
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
    wegnalDetail() {
      this.detailToggle = !this.detailToggle
    },
    googlePlayBtn() {
      document.getElementById('wegnalAos').click()
    },
    appStoreBtn() {
      document.getElementById('wegnalIos').click()
    }
  }
}
</script>

<style scoped lang="scss">
.wrap-project-card {
  background: white;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 15px;
  padding: 20px 20px;
  .wrap-detail-btn {
    display: flex;
    cursor: pointer;
    margin-top: 16px;
  }
  .item-type {
    padding-right: 20px;
    width: 100px;
    text-align: end !important;
  }
  h2 {
    font-size: 2.4rem;
  }
  p {
    font-size: 1.9rem;
    margin-bottom: 8px;
    color: $grey;
  }
  a {
    font-size: 1.9rem;
  }
  strong {
    font-size: 2rem;
    color: $grey;
  }
}
</style>
