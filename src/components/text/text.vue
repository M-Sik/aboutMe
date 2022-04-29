<template>
  <v-card-text
    :style="`font-size: ${fontSize}px;`"
    class="pa-0 textColor"
  >
    {{ textValue }}
  </v-card-text>
</template>

<script>
export default {
  name: 'NomalText',
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
