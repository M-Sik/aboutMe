<template>
  <v-row no-gutters>
    <v-col
      cols="auto"
      class="pr-5"
    >
      <v-icon
        color="black"
        size="50"
      >
        {{ iconName }}
      </v-icon>
    </v-col>
    <v-col cols="auto">
      <BoldText
        :text-value="firstTitle"
        font-size="24"
      />
      <NomalText
        :text-value="secondTitle"
        font-size="20"
      />
      <NomalText
        :text-value="thirdTitle"
        font-size="20"
      />
      <NomalText
        :text-value="fourthTitle"
        font-size="20"
      />
    </v-col>
  </v-row>
</template>

<script>
import BoldText from '@/components/text/textBold.vue'
import NomalText from '@/components/text/text.vue'

export default {
  name: "ItemForm",
  components: {
    NomalText,
    BoldText,
  },
  props: {
    iconName: {
      type: String,
      default: null
    },
    firstTitle: {
      type: String,
      default: "",
    },
    secondTitle: {
      type: String,
      default: "",
    },
    thirdTitle: {
      type: String,
      default: "",
    },
    fourthTitle: {
      type: String,
      default: "",
    }
  },
}
</script>

<style>

</style>
