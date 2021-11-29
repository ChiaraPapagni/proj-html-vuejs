<template>
  <main id="site_main">
    <About id="about" />

    <Services id="services" />

    <Process id="process" />

    <Team id="team" />

    <Blog id="blog" />

    <Newsletter id="newsletter" />
  </main>
  <!-- /#site_main -->
</template>

<script>
import About from "./About.vue";
import Services from "./Services.vue";
import Process from "./Process.vue";
import Team from "./Team.vue";
import Blog from "./Blog.vue";
import Newsletter from "./Newsletter.vue";

export default {
  components: {
    About,
    Services,
    Process,
    Team,
    Blog,
    Newsletter,
  },
};
</script>

<style lang="scss">
</style>