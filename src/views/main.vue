<template>
  <v-app>
    <MainAppBar />
    <v-main
      class="meBackground pa-0"
    >
      <v-row
        :style="`height: 100%;  padding-top: 64px;`"
        no-gutters
        justify="center"
      >
        <v-col>
          <Profile v-animate-css="mainFadeIn" />
          <v-divider style="border: solid 1px #6D6A6A; margin: 0px 160px;" />
          <AboutMe id="aboutMeSection" />
          <v-divider style="border: solid 1px #6D6A6A; margin: 0px 160px;" />
          <Skills id="skillsSection" />
        </v-col>
      </v-row>
      <ScrollUpBtn />
    </v-main>
    <v-divider
      id="test3"
      style="border: solid 1px #6D6A6A; margin: 0px 160px;"
    />
  </v-app>
</template>

<script>
import MainAppBar from '@/components/appBar/mainAppBar.vue'
import Profile from '@/components/profile/profile.vue'
import AboutMe from '@/components/aboutMe/aboutMe.vue'
import Skills from '@/components/skills/skills.vue'
import ScrollUpBtn from '@/components/button/scrollUpBtn'
// import NomalText from '@/components/text/text.vue'
// import BoldText from '@/components/text/textBold.vue'

export default {
  components: {
    MainAppBar,
    Profile,
    AboutMe,
    Skills,
    ScrollUpBtn
    // NomalText,
    // BoldText
  },
  data: () => ({
    clientWidth: 0,
    mainFadeIn: {
      classes: 'fadeIn',
      duration: 2000
    },
    // aboutMe태크 top값
    aboutMeH: null,
    // skills태그 top값
    skillsH: null,

  }),
  created() {
    // this.clientWidth = document.documentElement.clientWidth
  },
  mounted() {
    window.scrollTo(0, 0)
    document.addEventListener('scroll', this.scrollEvents);

    this.aboutMeH = document.getElementById("aboutMeSection").getBoundingClientRect().top;
    this.skillsH = document.getElementById("skillsSection").getBoundingClientRect().top;
  },
  destroyed() {
    document.removeEventListener('scroll', this.scrollEvents)
  },
  methods: {
    scrollEvents() {
      let totalH = document.documentElement.scrollHeight
      let scrollH = document.documentElement.scrollTop
      let contentH = this.$vuetify.breakpoint.height

      console.log(totalH, scrollH, contentH, this.aboutMeH, this.skillsH)
      if((scrollH + contentH) > this.aboutMeH) {
        if((scrollH + contentH) < this.skillsH) {
          // aboutMe 애니매이션 작동 id를 넣어서 click 이벤트 달면 될듯
        }
      }
      if((scrollH + contentH) > this.skillsH) {
        // skills 태그 애니매이션 작동 id를 넣어서 click 이벤트 달면 될듯
      }
    }
  }
};
</script>

<style>

</style>
