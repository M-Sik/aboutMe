<template>
  <div class="bg-color">
    <MainAppBar
      :about-me-toggle="headerAboutMeToggle"
      :skills-toggle="headerSkillsToggle"
      :projects-toggle="headerProjectsToggle"
      @click-about-me="clickAboutMe"
      @click-skills="clickSkills"
      @click-projects="clickProjects"
    />

    <v-row
      no-gutters
      justify="center"
    >
      <v-col>
        <Profile
          v-if="!$vuetify.breakpoint.mobile"
          v-animate-css="mainFadeIn"
        />
        <MProfile
          v-else
          v-animate-css="mainFadeIn"
        />
        <v-divider class="h1-divider" />
        <AboutMe
          v-if="!$vuetify.breakpoint.mobile"
          id="aboutMeSection"
        />
        <MAboutMe
          v-else
          id="aboutMeSection"
        />
        <v-divider class="h1-divider" />
        <Skills
          v-if="!$vuetify.breakpoint.mobile"
          id="skillsSection"
        />
        <MSkills
          v-else
          id="skillsSection"
        />
        <v-divider class="h1-divider" />
        <Projects
          v-if="!$vuetify.breakpoint.mobile"
          id="projectsSection"
        />
        <MProjects
          v-else
          id="projectsSection"
        />
      </v-col>
    </v-row>
    <ScrollUpBtn v-show="scrollUpBtnToggle" />
  </div>
</template>

<script>
import MainAppBar from '@/components/appBar/mainAppBar.vue'
import Profile from '@/components/profile/profile.vue'
import AboutMe from '@/components/aboutMe/aboutMe.vue'
import Skills from '@/components/skills/skills.vue'
import ScrollUpBtn from '@/components/button/scrollUpBtn'
import Projects from '@/components/projects/projects.vue'
import MProfile from '@/components/profile/m.profile.vue'
import MAboutMe from '@/components/aboutMe/m.aboutMe.vue'
import MSkills from '@/components/skills/m.skills.vue'
import MProjects from '@/components/projects/m.projects.vue'

export default {
  components: {
    MainAppBar,
    Profile,
    AboutMe,
    Skills,
    ScrollUpBtn,
    Projects,
    MProfile,
    MAboutMe,
    MSkills,
    MProjects,
  },
  data: () => ({
    scrollUpBtnToggle: false,
    headerAboutMeToggle: true,
    headerSkillsToggle: false,
    headerProjectsToggle: false,
    // aboutMe태크 top값
    aboutMeH: null,
    // skills태그 top값
    skillsH: null,
    // projects 태그 top 값
    projectsH: null,
    // 애니메이션
    mainFadeIn: {
      classes: 'fadeIn',
      duration: 2000
    },
  }),
  mounted() {
    window.scrollTo(0, 0)
    document.addEventListener('scroll', this.scrollEvents);

    this.aboutMeH = document.getElementById("aboutMeSection").getBoundingClientRect().top;
    this.skillsH = document.getElementById("skillsSection").getBoundingClientRect().top;
    this.projectsH = document.getElementById("projectsSection").getBoundingClientRect().top;
  },
  destroyed() {
    document.removeEventListener('scroll', this.scrollEvents)
  },
  methods: {
    scrollEvents() {
      let scrollH = document.documentElement.scrollTop
      let contentH = this.$vuetify.breakpoint.height

      if((scrollH + contentH) > this.aboutMeH) {
        // about me 영역
        if((scrollH + contentH) < this.skillsH) {
          this.headerAboutMeToggle = true
          this.headerSkillsToggle = false
          this.headerProjectsToggle = false
        }
        // skills 영역
        if((scrollH + contentH) > this.skillsH) {
          if((scrollH + contentH) < this.projectsH){
            // 상단으로 보내는 스크롤 버튼
            this.scrollUpBtnToggle = true
            // skills 태그 애니매이션 작동 id를 넣어서 click 이벤트 달면 될듯
            this.headerAboutMeToggle = false
            this.headerSkillsToggle = true
            this.headerProjectsToggle = false
          }
        }
        // projects 영역
        if((scrollH + contentH) > this.projectsH) {
          // 상단으로 보내는 스크롤 버튼
          this.scrollUpBtnToggle = true
          // skills 태그 애니매이션 작동 id를 넣어서 click 이벤트 달면 될듯
          this.headerAboutMeToggle = false
          this.headerSkillsToggle = false
          this.headerProjectsToggle = true
        }
      }else{
        this.scrollUpBtnToggle = false
        this.headerAboutMeToggle = true
        this.headerSkillsToggle = false
        this.headerProjectsToggle = false
      }
    },
    clickAboutMe() {
      window.scrollTo({top: this.aboutMeH - 220, left: 0, behavior: 'smooth'})
    },
    clickSkills() {
      window.scrollTo({top: this.skillsH - 220, left: 0, behavior: 'smooth'})
    },
    clickProjects() {
      window.scrollTo({top: this.projectsH - 100, left: 0, behavior: 'smooth'})
    }
  }
};
</script>

<style scoped lang="scss">
</style>
