<template>
  <v-app-bar
    elevation="0"
    class="meBackground px-6"
    fixed
  >
    <v-row
      justify="space-between"
      style="height: 100%"
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
          v-show="!$vuetify.breakpoint.mobile"
          :class="{greyColorText: aboutMeToggle===false, blackColorText: aboutMeToggle===true}"
          text-value="AboutMe"
          font-size="24"
          @click.native="clickAboutMe"
        />
        <NomalText
          v-show="!$vuetify.breakpoint.mobile"
          :class="{greyColorText: skillsToggle===false, blackColorText: skillsToggle===true}"
          text-value="Skills"
          font-size="24"
          style="color: #727070"
          @click.native="clickSkills"
        />
        <NomalText
          v-show="!$vuetify.breakpoint.mobile"
          text-value="Projects"
          font-size="24"
          :class="{greyColorText: projectsToggle===false, blackColorText: projectsToggle===true}"
          @click.native="clickProjects"
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
