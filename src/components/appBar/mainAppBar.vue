<template>
  <v-app-bar
    v-if="!$vuetify.breakpoint.mobile"
    elevation="0"
    class="meBackground px-6"
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
        <v-row no-gutters>
          <v-col
            cols="auto"
            class="pr-3"
          >
            <BoldText
              text-value="dev_sik"
              font-size="32"
            />
          </v-col>
          <v-col
            cols="auto"
            class="pt-2"
          >
            <NomalText
              text-value="front-end developer"
              style="color: #727070"
              font-size="24"
            />
          </v-col>
        </v-row>
      </v-col>
      <v-col
        style="display: flex;"
        cols="auto"
      >
        <NomalText
          :class="{greyColorText: aboutMeToggle===false, blackColorText: aboutMeToggle===true}"
          text-value="AboutMe"
          font-size="24"
          @click.native="clickAboutMe"
        />
        <NomalText
          :class="{greyColorText: skillsToggle===false, blackColorText: skillsToggle===true}"
          text-value="Skills"
          font-size="24"
          style="color: #727070"
          @click.native="clickSkills"
        />
        <NomalText
          text-value="Projects"
          font-size="24"
          :class="{greyColorText: projectsToggle===false, blackColorText: projectsToggle===true}"
          @click.native="clickProjects"
        />
      </v-col>
    </v-row>
  </v-app-bar>
  <!-- 테블릿, 모바일일때 -->
  <v-app-bar
    v-else
    style="width: 100vw;"
    elevation="0"
    class="meBackground pl-2"
    fixed
  >
    <v-row
      align="center"
      no-gutters
    >
      <v-col cols="auto">
        <BoldText
          class="pr-1"
          text-value="dev_sik"
          font-size="16"
        />
      </v-col>
      <v-col cols="auto">
        <NomalText
          class="mt-1"
          text-value="front-end developer"
          style="color: #727070"
          font-size="14"
        />
      </v-col>
    </v-row>
  </v-app-bar>
</template>

<script>
import NomalText from '@/components/text/text.vue'
import BoldText from '@/components/text/textBold.vue'
export default {
  name: "MainAppBar",
  components: {
    NomalText,
    BoldText
  },
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

<style scoped>
.greyColorText {
  color: #727070 !important;
  padding-right: 52px !important;
}
.blackColorText {
  color: black !important;
  padding-right: 52px !important;
}
</style>
