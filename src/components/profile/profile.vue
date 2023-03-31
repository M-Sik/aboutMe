<template>
  <section>
    <v-row
      no-gutters
      class="vh-100"
      justify="center"
      align="center"
    >
      <v-col
        cols="auto"
        class="pr-10"
      >
        <v-img
          class="wrap-img"
          src="@/assets/images/profileImg.png"
        />
      </v-col>
      <v-col
        align-self="center"
        cols="auto"
      >
        <p>
          안녕하세요☺️
          <br>
          프로그래밍이라는 게임을 즐기며
          <br>
          스타트업에서 일하고있는 2년차
          <br>
          ✌️Front-End 개발자 김명식 입니다.✌
        </p>
      </v-col>
    </v-row>
  </section>
</template>

<script>
export default {
  name: "Profile",
}
</script>

<style scoped lang="scss">
.wrap-img {
  width: 25vw;
}
p {
  font-size: 3.2rem;
  font-weight: 700;
  color: $grey;
}
</style>
