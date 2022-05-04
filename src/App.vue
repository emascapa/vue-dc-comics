<template>
  <div id="app">
    <SiteHeader />
    <SiteMain />
    <SiteSection />
    <SiteFooter />
  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue' */
import SiteHeader from "@/components/HeaderComponent.vue";
import SiteMain from "@/components/MainComponent.vue";
import SiteSection from "@/components/SectionComponent.vue";
import SiteFooter from "@/components/FooterComponent.vue";


export default {
  name: "App",
  components: {
    SiteHeader,
    SiteMain,
    SiteSection,
    SiteFooter,
    //SiteUpperFooter,
    //SiteLowerFooter,
  },
};
</script>

<style lang="scss">
@import "@/assets/sass/style.scss";

/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
