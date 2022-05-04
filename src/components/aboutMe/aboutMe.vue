<template>
  <v-card
    style="
      background: #FFFDFD;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 15px;
      margin: 0px 220px;
      padding: 50px 60px;
    "
  >
    <v-row
      justify="center"
      style="padding-bottom: 60px;"
      no-gutters
    >
      <v-col cols="auto">
        <BoldText
          text-value="ABOUT ME"
          font-size="32"
        />
      </v-col>
    </v-row>
    <v-row
      justify="space-between"
      no-gutters
    >
      <v-col cols="auto">
        <ItemForm
          class="mb-9"
          icon-name="mdi-account-outline"
          first-title="이름"
          second-title="김명식"
        />
        <ItemForm
          class="mb-9"
          icon-name="mdi-post-outline"
          first-title="블로그"
          second-title="sikk.tistory.com"
        />
        <ItemForm
          class="mb-9"
          icon-name="mdi-account-school-outline"
          first-title="학력"
          second-title="서원대학교 2021.02 졸업"
          third-title="(정보통신공학)"
          fourth-title="학점: 3.94/4.5"
        />
      </v-col>
      <v-col cols="auto">
        <ItemForm
          class="mb-9"
          icon-name="mdi-cake-variant-outline"
          first-title="생년월일"
          second-title="97.01.13"
        />
        <ItemForm
          class="mb-9"
          icon-name="mdi-email-outline"
          first-title="이메일"
          second-title="rlaaudtlr233@gmail.com"
        />
        <ItemForm
          class="mb-9"
          icon-name="mdi-account-details-outline"
          first-title="경력"
          second-title="주식회사 느루(2021.09 ~ 재직중)"
          third-title="담당업무 : front-end개발"
        />
      </v-col>
      <v-col cols="auto">
        <ItemForm
          class="mb-9"
          icon-name="mdi-phone-outline"
          first-title="연락처"
          second-title="010-5754-7220"
        />
        <ItemForm
          class="mb-9"
          icon-name="mdi-card-account-details-outline"
          first-title="자격증"
          second-title="정보처리기사"
        />
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'
import ItemForm from '@/components/aboutMe/itemForm.vue'

export default {
  name: 'AboutMe',
  components: {
    // NomalText,
    BoldText,
    ItemForm
  },
}
</script>

<style>

</style>
