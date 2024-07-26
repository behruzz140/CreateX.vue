<template>
  <Header />
  <CarouselPage />
  <Construction />
  <ServicePage />
  <!-- <Footer /> -->

</template>
<script>
import Header from "./components/Header/Header.vue";
import Footer from "./components/Footer/Footer.vue";
import CarouselPage from "./components/Caousel/carousel.vue";
import Construction from "./components/Construction/construction.vue";
import ServicePage from "./components/ServicePage/services.vue";
export default {
  name: "App",
  components: {
    Header,
    Footer,
    CarouselPage,
    Construction,
     ServicePage,

  }
};

</script>
<style scoped>
* {
  color: #000;
}
</style>
