<template>
  <div id="app">
    <SiteHeader/>
    <SiteMain/>
    <SiteSection/>
    <SiteUpperFooter/>
    <SiteLowerFooter/>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue' */
import SiteHeader from '@/components/HeaderComponent.vue'
import SiteMain from '@/components/MainComponent.vue'
import SiteSection from '@/components/SectionComponent.vue'
import SiteUpperFooter from '@/components/UpperFooterComponent.vue'
import SiteLowerFooter from '@/components/LowerFooterComponent.vue'

export default {
  name: 'App',
  components: {
    SiteHeader,
    SiteMain,
    SiteSection,
    SiteUpperFooter,
    SiteLowerFooter,
  }
}
</script>

<style lang="scss">

@import '@/assets/sass/style.scss';

/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
