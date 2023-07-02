<template>
  <nav-menu></nav-menu>
  <home-card></home-card>
  <gallery id="gallery"></gallery>
  <volunteers-card id="volunteers"></volunteers-card>
  <contactCard id="contact"></contactCard>
</template>

<script>
    import NavMenu from "@/components/NavMenu.vue";
    import HomeCard from "@/components/HomeCard.vue";
    import VolunteersCard from "@/components/volunteersCard.vue";
    import ContactCard from "@/components/contactCard.vue";
    import Gallery from "@/components/gallery.vue";
    export default {
        name: "MainView",
        components: {Gallery, VolunteersCard, HomeCard, NavMenu, ContactCard}
    }
</script>

<style scoped>

</style>
