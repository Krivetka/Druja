<template>
<div class="gallery-field">
  <div class="wrapper">
    <img class="box box1" src="@/assets/photo/20.jpg">
    <img class="box box2" src="@/assets/photo/13.jpg">
    <img class="box box3" src="@/assets/photo/5.jpg">
    <img class="box box4" src="@/assets/photo/3.jpg">
    <img class="box box5" src="@/assets/photo/8.jpg">
    <img class="box box6" src="@/assets/photo/9.jpg">
    <img class="box box7" src="@/assets/photo/4.jpg">
    <img class="box box8" src="@/assets/photo/18.jpg">
    <img class="box box9" src="@/assets/photo/5.jpg">
    <img class="box box10" src="@/assets/photo/15.jpg">
    <img class="box box11" src="@/assets/photo/19.jpg">
    <img class="box box12" src="@/assets/photo/20.jpg">
    <img class="box box13" src="@/assets/photo/13.jpg">
    <img class="box box14" src="@/assets/photo/5.jpg">
    <img class="box box15" src="@/assets/photo/3.jpg">
    <img class="box box16" src="@/assets/photo/8.jpg">
    <img class="box box17" src="@/assets/photo/9.jpg">
    <img class="box box18" src="@/assets/photo/4.jpg">
    <img class="box box19" src="@/assets/photo/18.jpg">
    <img class="box box20" src="@/assets/photo/5.jpg">
    <img class="box box21" src="@/assets/photo/15.jpg">
    <img class="box box22" src="@/assets/photo/19.jpg">
  </div>
</div>
</template>

<script>
export default {
  name: "gallery"
}
</script>

<style scoped>
.gallery-field{
  display: flex;
  height: 100vh;
  width: 100%;
  align-items: center;
  justify-content: center;
}
.wrapper {
  width: 72vw;
  height: 36vw;
  display: grid;
  grid-template-columns: repeat(8, 9vw);
  grid-template-rows: repeat(4, 9vw);
  gap: 0.4vw;
}
.box {
  width: 100%;
  height: 100%;
  object-fit: cover;
  box-shadow: 4px 4px 8px 0px rgba(0, 0, 0, 0.3);
}
.box2 {
  grid-column: 2 / 4;
  grid-row: 1;
}
.box7{
  grid-column: 6 / 8;
  grid-row: 1 / 3;
}
.box8{
  grid-column: 3 / 5;
  grid-row: 3 / 5;
}
.box11{
  grid-column: 1 / 2;
  grid-row: 2 / 4;
}
.box12{
  grid-column: 5 / 7;
  grid-row: 3 / 3;
}
.box16{
  grid-column: 7 / 9;
  grid-row: 4 / 4;
}
</style>