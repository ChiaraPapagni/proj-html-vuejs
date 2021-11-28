<template>
  <main id="site_main">
    <About id="about" />

    <Services id="services" />

    <Process id="process" />

    <Team id="team" />

    <Blog id="blog" />

    <div id="newsletter" class="newsletter">
      <div class="d_flex">
        <div class="know col">
          <div class="section_title">{{ sectionTitle }}</div>
          <h2>
            <span class="title_bg">{{ title.marked }}</span>
            {{ title.notMarked }}
          </h2>
          <p>
            {{ description }}
          </p>
        </div>
        <!-- /.know -->

        <div class="form col">
          <input type="text" placeholder="Name" class="input" />
          <input type="text" placeholder="Email" class="input" />
          <div class="btn">subscribe</div>
        </div>
        <!-- /.form -->
      </div>
    </div>
    <!-- /.newsletter -->
  </main>
  <!-- /#site_main -->
</template>

<script>
import About from "./About.vue";
import Services from "./Services.vue";
import Process from "./Process.vue";
import Team from "./Team.vue";
import Blog from "./Blog.vue";

export default {
  components: {
    About,
    Services,
    Process,
    Team,
    Blog,
  },
  data() {
    return {
      sectionTitle: "Newsletter",
      title: {
        marked: "Know",
        notMarked: "First",
      },
      description: `Follow closely and receive content about our company and the news of
            the current market.`,
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

main {
  .newsletter {
    background-image: url("../assets/img/bg-1.jpg");
    background-position-y: center;
    background-attachment: fixed;
    object-position: center;
    padding: 130px 0;
    color: $nexgen_light_grey_text;
    font-weight: 300;

    & > .d_flex {
      width: 50%;
      margin: auto;
      gap: 2rem;
    }

    .know {
      h2 {
        color: $nexgen_white;
        margin: 1rem 0;

        .title_bg {
          background-color: rgba($nexgen_primary_color, 0.2);
        }
      }
    }
  }
}
</style>