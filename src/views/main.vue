<template>
  <v-app>
    <MainAppBar
      :about-me-toggle="headerAboutMeToggle"
      :skills-toggle="headerSkillsToggle"
      :projects-toggle="headerProjectsToggle"
      @click-about-me="clickAboutMe"
      @click-skills="clickSkills"
      @click-projects="clickProjects"
    />
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
          <AboutMe
            id="aboutMeSection"
            v-animate-css.click="aboutMeAnimation"
          />
          <v-divider style="border: solid 1px #6D6A6A; margin: 0px 160px;" />
          <Skills
            id="skillsSection"
            v-animate-css.click="skillsAnimation"
          />
        </v-col>
      </v-row>
      <ScrollUpBtn v-show="scrollUpBtnToggle" />
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
    scrollUpBtnToggle: false,
    headerAboutMeToggle: true,
    headerSkillsToggle: false,
    headerProjectsToggle: false,
    aboutMeAniVal: 0,
    skilsAniVal: 0,
    // aboutMe태크 top값
    aboutMeH: null,
    // skills태그 top값
    skillsH: null,
    // 애니메이션
    mainFadeIn: {
      classes: 'fadeIn',
      duration: 2000
    },
    aboutMeAnimation: {
      classes: 'tada',
      delay: 500,
      duration: 2000
    },
    skillsAnimation: {
      classes: 'fadeInLeft'
    }
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
        // about me 영역
        if((scrollH + contentH) < this.skillsH) {
          // 애니메이션 변수 초기화
          this.skilsAniVal = 0 // 스킬 애니메이션
          // 애니메이션은 한번만 작동해야하기에 조건문 걸어놈
          if(this.aboutMeAniVal < 1) {
            document.getElementById('aboutMeSection').click();
            this.aboutMeAniVal++
          }
          this.headerAboutMeToggle = true
          this.headerSkillsToggle = false
          this.headerProjectsToggle = false
          console.log("어바웃미")
        }
        if((scrollH + contentH) > this.skillsH) {
          // 애니메이션을 위한 변수 초기화
          this.aboutMeAniVal = 0 // 어바웃미 애니메이션 변수
          // 애니메이션은 한번만 작동해야하기에 조건문 걸어놈
          if(this.skilsAniVal < 1) {
            document.getElementById('skillsSection').click();
            this.skilsAniVal++
          }
          // 상단으로 보내는 스크롤 버튼
          this.scrollUpBtnToggle = true
          // skills 태그 애니매이션 작동 id를 넣어서 click 이벤트 달면 될듯
          this.headerAboutMeToggle = false
          this.headerSkillsToggle = true
          this.headerProjectsToggle = false
          console.log("스킬")
        }
      }else{
        // 애니메이션 변수 초기화
        this.skilsAniVal = 0 // 스킬 애니메이션
        this.aboutMeAniVal = 0 // 어바웃미 애니메이션

        this.scrollUpBtnToggle = false
        this.headerAboutMeToggle = true
        this.headerSkillsToggle = false
        this.headerProjectsToggle = false
      }
    },
    clickAboutMe() {
      console.log("어바웃미 클릭")
      window.scrollTo({top: this.aboutMeH - 70, left: 0, behavior: 'smooth'})
      // document.getElementById("aboutMeSection").scrollIntoView()
    },
    clickSkills() {
      console.log("스킬 클릭")
      window.scrollTo({top: this.skillsH - 70, left: 0, behavior: 'smooth'})
    },
    clickProjects() {
      console.log("프로젝트 클릭")
    }
  }
};
</script>

<style>

</style>
