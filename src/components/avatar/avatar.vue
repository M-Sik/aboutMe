<template>
  <v-avatar
    width="430px"
    height="430px"
  >
    <img :src="imgSrc">
  </v-avatar>
</template>

<script>
export default {
  name: "AvatarImg",
  props: {
    imgSrc: {
      type: String,
      default: null
    }
  }
}
</script>

<style>

</style>
