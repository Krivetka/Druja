<template xmlns="http://www.w3.org/1999/html">
  <div class="card">
    <div class="left-card">
      <h2 class="left-card__title">
        Кантакты ................. .................. для ............ ......................... сувязі
      </h2>
      <h2 class="left-card__subtitle">
        <span class="bold-text">+375 29 283 83 60 &nbsp;</span> айцец Ігар &nbsp;&mdash;&nbsp; па агульным пытанням
        <br><br>
        <span class="bold-text">+375 33 678 95 59 &nbsp;</span> Алесь &nbsp;&mdash;&nbsp;
        арганізацыя экскурсій, праектная і культурная дзейнасць
        <br><br>
        <span class="bold-text">+375 29 810 54 00 &nbsp;</span> Дзімітрый &nbsp;&mdash;&nbsp;
        пражыванне, партнерскія прапановы, гаспадарчая
        дзейнасць
        <br><br>
        <span class="bold-text">borders.secrets@gmail.com</span>
        <br>
        <br>
        211960 Віцебская вобласць, Браслаўскі раён,<br>
        аг. Друя, вул. Альтэра Друянава 16
        <br>
        <br>
        Валанцёрскаe аб’яднаннe <span class="bold-text"> “Таямніцы пры граніцы”</span>
      </h2>

    </div>
    <div class="curve"></div>
    <div class="right-card">
      <img src="@/assets/photo/23.jpg" class="right-card__img"/>
      <icon-wave class="wave"></icon-wave>
    </div>
  </div>
</template>

<script>
import IconWave from "@/components/icons/IconWave.vue";

export default {
  name: "contactCard",
  components: {IconWave }
}
</script>

<style scoped>
.card {
  display: flex;
  height: 100vh;
  width: 100%;
  position: relative;
  overflow: hidden;
}

.left-card {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 50%;
  height: 100%;
  position: relative;
}

.left-card__title {
  width: 54%;
  margin-bottom: 2vw;
  font-family: 'Montserrat', sans-serif;
  font-weight: 400;
  font-size: 2.8vw;
  line-height: 1;
  color: black;
  margin-left: -4%;
}

.left-card__subtitle {
  width: 48%;
  font-family: 'Montserrat', sans-serif;
  font-weight: 400;
  font-size: 0.8vw;
  line-height: 1.4vw;
  margin-left: -10%;
  margin-bottom: 5vh;
}

.bold-text {
  font-weight: 900;
}

.right-card {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 50%;
}

.wave {
  position: absolute;
  height: 100%;
  left: 0;
  top: 0;
  transform: scale(-1, -1);
}

.right-card__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>