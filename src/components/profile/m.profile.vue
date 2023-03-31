<template>
  <section>
    <v-row
      align="center"
      justify="center"
      no-gutters
      class="vh-100"
    >
      <v-col cols="auto">
        <v-row
          justify="center"
          no-gutters
        >
          <v-col cols="auto">
            <v-img
              class="wrap-img"
              src="@/assets/images/profileImg.png"
            />
          </v-col>
        </v-row>
        <div class="mt-4">
          <p>
            안녕하세요☺️
            <br>
            프로그래밍이라는 게임을 즐기며
            <br>
            스타트업에서 일하고있는 2년차
            <br>
            ✌️Front-End 개발자 김명식 입니다.✌
          </p>
        </div>
      </v-col>
    </v-row>
  </section>
</template>

<script>
export default {
  name: "MProfile",
}
</script>

<style scoped lang="scss">
.wrap-img {
  width: 60vw;
}
p {
  font-size: 3.2rem;
  text-align: center;
  font-weight: 700;
}
</style>
