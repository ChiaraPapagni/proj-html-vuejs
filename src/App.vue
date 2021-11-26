<template>
  <div id="app">
    <SiteHeader :phone="phone" :email="email" :openHours="openHours" />
    <SiteMain />
    <SiteFooter :phone="phone" :email="email" :address="address" />
  </div>
</template>

<script>
import SiteHeader from "./components/SiteHeader.vue";
import SiteMain from "./components/SiteMain.vue";
import SiteFooter from "./components/SiteFooter.vue";

export default {
  name: "App",
  components: {
    SiteMain,
    SiteHeader,
    SiteFooter,
  },
  data() {
    return {
      phone: "+1 (305) 1234-5678",
      email: "hello@example.com",
      address: "Main Avenue, 987",
      openHours: {
        days: "Mon - Sat",
        hours: "9.00 - 18.00",
      },
    };
  },
};
</script>

<style lang="scss">
@import "./assets/scss/variables.scss";
@import "./assets/scss/common.scss";
</style>
