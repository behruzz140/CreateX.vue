<template>
  <Header />
  <CarouselPage />
  <Construction />
  <ServicePage />
  <Buildings />
  <Partners />
  <Facts />
  <Discussion />
  <Footer />

</template>
<script>
import Header from "./components/Header/Header.vue";
import Footer from "./components/Footer/footer.vue";
import CarouselPage from "./components/Caousel/carousel.vue";
import Construction from "./components/Construction/construction.vue";
import ServicePage from "./components/ServicePage/services.vue";
import Buildings from "./components/Buildings/buildings.vue";
import Partners from "./components/Partners/partners.vue";
import Facts from "./components/Facts/facts.vue";
import Discussion from './components/Discussion/discussion.vue';
export default {
  name: "App",
  components: {
    Header,
    Footer,
    CarouselPage,
    Construction,
    ServicePage,
    Buildings,
    Partners,
    Facts,
    Discussion,
  }
};

</script>
<style scoped>
* {
  color: #000;
}
</style>
