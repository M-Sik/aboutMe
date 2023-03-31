<template>
  <!-- 웹 -->
  <v-app-bar
    v-if="!$vuetify.breakpoint.mobile"
    elevation="0"
    class="bg-color px-6"
    fixed
  >
    <v-row
      justify="space-between"
      no-gutters
      align="center"
    >
      <v-col
        cols="auto"
      >
        <h2>dev_sik <span>Front-End Developer</span></h2>
      </v-col>
      <v-col
        style="display: flex;"
        cols="auto"
      >
        <nav
          :class="aboutMeToggle ? 'black--text' : ''"
          @click="clickAboutMe"
        >
          AboutMe
        </nav>
        <nav
          :class="skillsToggle ? 'black--text' : ''"
          @click="clickSkills"
        >
          Skills
        </nav>
        <nav
          :class="projectsToggle ? 'black--text' : ''"
          @click="clickProjects"
        >
          Projects
        </nav>
      </v-col>
    </v-row>
  </v-app-bar>
  <!--  -->
  <!-- 테블릿, 모바일일때 -->
  <v-app-bar
    v-else
    style="width: 100vw;"
    elevation="0"
    class="bg-color pl-2"
    fixed
  >
    <h2>dev_sik <span>Front-End Developer</span></h2>
  </v-app-bar>
</template>

<script>
export default {
  name: "MainAppBar",
  props: {
    aboutMeToggle: {
      type: Boolean,
      default: null
    },
    skillsToggle: {
      type: Boolean,
      default: null
    },
    projectsToggle: {
      type: Boolean,
      default: null
    },
  },
  methods: {
    clickAboutMe() {
      this.$emit('click-about-me')
    },
    clickSkills() {
      this.$emit('click-skills')
    },
    clickProjects() {
      this.$emit('click-projects')
    }
  }
};
</script>

<style scoped lang="scss">
h2 {
  font-size: 3.2rem;
  span {
    font-size: 2.4rem;
    color: $grey-light-1;
  }
}
nav {
  padding-right: 52px;
  font-size: 2.4rem;
  color: $grey-light-1;
  cursor: pointer;
}
</style>
