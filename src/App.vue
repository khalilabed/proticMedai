<template>
  <header-page></header-page>
  <hero-section></hero-section>
  <page-body></page-body>
  <form-page></form-page>
  <footer-page></footer-page>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import HeaderPage from "./components/HeaderPage.vue";
import HeroSection from "./components/HeroSection.vue";
import PageBody from "./components/PageBody.vue";
import FormPage from "./components/FormPage.vue";
import FooterPage from "./components/FooterPage.vue";

export default {
  name: "App",
  components: {
    HeaderPage,
    HeroSection,
    FooterPage,
    PageBody,
    FormPage
  },
};
</script>

<style>
</style>
