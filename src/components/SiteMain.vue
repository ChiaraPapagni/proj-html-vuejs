<template>
  <main id="site_main">
    <div class="company">
      <div class="container d_flex">
        <div class="col">
          <p class="title">about the network</p>
          <h3><span class="title_bg">The</span> Company</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cras
            iaculis diam varius diam ultricies lacina. Mauris lacus tellus,
            ultrices eu volutpat sit amet, finibus a ipsum.
          </p>
          <p>
            Curabitur convallis, diam a egestas iaculis, neque lorem interdum
            falis, in viverra lacus tortor in leo.
          </p>
        </div>
        <div class="col d_flex">
          <div class="col">
            <h4>
              <font-awesome-icon
                :icon="['fas', 'medal']"
                class="icon"
              />Tradition
            </h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>

            <h4>
              <font-awesome-icon
                :icon="['far', 'edit']"
                class="icon"
              />Certificate
            </h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <div class="col">
            <h4>
              <font-awesome-icon
                :icon="['fas', 'unlock-alt']"
                class="icon"
              />Security
            </h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
            <h4>
              <font-awesome-icon
                :icon="['fas', 'graduation-cap']"
                class="icon"
              />Expertise
            </h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
        </div>
      </div>
    </div>
    <!-- /.company -->

    <Services />
    <!-- /.services -->

    <div class="management"></div>
    <!-- /.management -->

    <div class="team"></div>
    <!-- /.team -->

    <div class="news"></div>
    <!-- /.news -->

    <div class="newsletter"></div>
    <!-- /.newsletter -->
  </main>
  <!-- /#site_main -->
</template>

<script>
import Services from "./Services.vue";
export default {
  components: {
    Services,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

main {
  .company {
    background-color: $nexgen_bg_dark;
    padding: 120px 0;
    color: #ccc;
    font-weight: 300;

    .container {
      align-items: end;
      gap: 6.5rem;

      h3 {
        color: white;
      }

      .title_bg {
        background-color: #0e272d;
      }

      p {
        margin: 1rem 0;
      }

      .icon {
        color: #00a6a6;
        font-size: 1.4rem;
        margin-right: 0.5rem;
      }

      h4 {
        color: white;
      }
    }
  }
}
</style>