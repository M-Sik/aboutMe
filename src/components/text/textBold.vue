<template>
  <v-card-text
    :style="`font-size: ${fontSize}px; font-weight: bold;`"
    class="font-weigth-bold pa-0 textColor"
  >
    {{ textValue }}
  </v-card-text>
</template>

<script>
export default {
  name: 'BoldText',
  props: {
    textValue: {
      type: String,
      default: null
    },
    fontSize: {
      type: String,
      default: null
    }
  }
}
</script>

<style scoped>
.textColor {
  color: #413F3F;
}
</style>
