<template>
  <nav class="nav">
    <img class="logo" src="@/assets/logo2.png" alt="logo">
    <div class="text-menu">
      <a class="text-menu__link">Аб нас</a>
      <a class="text-menu__link" href="#" v-scroll-to="'#gallery'">галерэя</a>
      <a class="text-menu__link" href="#" v-scroll-to="'#volunteers'">валанцёры</a>
      <a class="text-menu__link" href="#" v-scroll-to="'#contact'">кантакты</a>
      <a class="text-menu__link text-menu__phone"> + 375 (29) 283-83-60</a>
    </div>
  </nav>
</template>

<script>
    export default {
        name: "NavMenu"
    }
</script>

<style scoped>
  .nav{
    z-index: 3;
    display: flex;
    justify-content: space-between;
    width: calc(100% - 40px);
    margin: 10px 20px 0;
    position: absolute;
  }
  .text-menu {
    margin-top: 14px;
    margin-right: 5px;
  }
  .text-menu__phone {
    border: 1px solid #111111;
    border-radius: 5px;
    padding: 10px 15px;
  }
  .text-menu__link{
    margin-left: 40px;
    font-family: 'Montserrat', sans-serif;
    color: #111111;
    text-transform: uppercase;
    font-size: 1vw;
    cursor: pointer;
    text-decoration: none;
  }
  .logo{
    width: 6vw;
    filter: drop-shadow(5px 5px 50px rgba(10,10,10,0.8));
  }
</style>
