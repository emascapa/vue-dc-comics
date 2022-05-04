<template>
  <footer>
    <SiteUpperFooter/>
    <SiteLowerFooter/>
  </footer>
</template>

<script>
import SiteUpperFooter from "@/components/UpperFooterComponent.vue";
import SiteLowerFooter from "@/components/LowerFooterComponent.vue";

export default {
  name: "FooterComponent",
  components: {
    SiteUpperFooter,
    SiteLowerFooter,
  },
};
</script>