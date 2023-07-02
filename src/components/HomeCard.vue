<template>
  <div class="home">
    <div class="left-card">
      <img src="@/assets/photo/10.jpg" class="left-card__img" />
      <icon-wave class="wave"></icon-wave>
    </div>
    <div class="curve"></div>
    <div class="right-card">
      <h1 class="right-card__title">
        Таямнiцы .................. ................ пры .............. ......................
        граніцы
      </h1>
      <h2 class="right-card__subtitle">
        Валанцёрскае аб'яднанне неабыякавай моладзі, якая займаецца захаваннем і адраджэннем гісторыка-культурнай спадчыны вёскі Друя
      </h2>
      <div class="social-media">
        <a class="social-media__logo" href="https://www.instagram.com/borders.secrets/">
          <icon-vk></icon-vk>
        </a>
        <a class="social-media__logo" href="https://vk.com/tayamnic">
          <icon-instagram></icon-instagram
        ></a>
        <a
          class="social-media__logo"
          href="https://www.facebook.com/profile.php?id=100064518709798"
        >
          <icon-facebook></icon-facebook>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import IconFacebook from '@/components/icons/IconFacebook.vue'
import IconInstagram from '@/components/icons/IconInstagram.vue'
import IconVk from '@/components/icons/IconVk.vue'
import IconWave from '@/components/icons/IconWave.vue'
export default {
  name: 'HomeCard',
  components: { IconWave, IconVk, IconInstagram, IconFacebook }
}
</script>

<style scoped>
.home {
  display: flex;
  height: 100vh;
  width: 100%;
  position: relative;
  overflow: hidden;
}
.left-card {
  width: 52%;
  height: 100%;
  position: relative;
}
.left-card__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.right-card {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 48%;
}
.wave {
  position: absolute;
  height: 100%;
  right: 0;
  top: 0;
}
.right-card__title {
  width: 70%;
  margin-bottom: 2vw;
  font-family: 'Montserrat', sans-serif;
  font-weight: 400;
  font-size: 3.4vw;
  line-height: 1;
  color: black;
}
.right-card__subtitle {
  width: 70%;
  padding-bottom: 2.6vw;
  font-family: 'Montserrat', sans-serif;
  font-weight: 400;
  font-size: 1.2vw;
  line-height: 1.7vw;
}

.social-media {
  display: flex;
  justify-content: end;
  align-items: center;
  position: absolute;
  bottom: 0.6vw;
  right: 1vw;
}
.social-media__logo {
  fill: #000;
  color: #000;
}
.social-media__logo:nth-child(1) {
  margin-right: 1vw;
}
.social-media__logo:nth-child(2) {
  margin-right: 0.5vw;
}
</style>
