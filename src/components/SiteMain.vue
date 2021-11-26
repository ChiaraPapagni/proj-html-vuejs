<template>
  <main id="site_main">
    <div class="company">
      <div class="container d_flex">
        <div class="col">
          <p class="section_title">about the network</p>
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

    <Management />
    <!-- /.management -->

    <Team />
    <!-- /.team -->

    <News />
    <!-- /.news -->

    <div class="newsletter">
      <div class="d_flex">
        <div class="know col">
          <div class="section_title">Newsletter</div>
          <h3><span class="title_bg">Know</span> First</h3>
          <p>
            Follow closely and receive content about our company and the news of
            the current market.
          </p>
        </div>
        <!-- /.know -->

        <div class="form col">
          <input type="text" placeholder="Name" class="input" />
          <input type="text" placeholder="Email" class="input" />
          <div class="btn_green">subscribe</div>
        </div>
        <!-- /.form -->
      </div>
    </div>
    <!-- /.newsletter -->
  </main>
  <!-- /#site_main -->
</template>

<script>
import Services from "./Services.vue";
import Management from "./Management.vue";
import Team from "./Team.vue";
import News from "./News.vue";

export default {
  components: {
    Services,
    Management,
    Team,
    News,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

main {
  .company {
    background-color: $nexgen_primary_dark;
    padding: 120px 0;
    color: $nexgen_light_grey_text;
    font-weight: 300;

    .container {
      align-items: end;
      gap: 6.5rem;

      h3 {
        color: $nexgen_white;
      }

      .title_bg {
        background-color: rgba($nexgen_primary_green, 0.2);
      }

      p {
        margin: 1rem 0;
      }

      .icon {
        color: $nexgen_primary_green;
        font-size: 1.4rem;
        margin-right: 0.5rem;
      }

      h4 {
        color: $nexgen_white;
      }
    }
  }

  .newsletter {
    background-image: url("../assets/img/bg-1.jpg");
    background-position-y: center;
    object-position: center;
    padding: 120px 0;
    color: $nexgen_light_grey_text;
    font-weight: 300;

    & > .d_flex {
      width: 50%;
      margin: auto;
      gap: 2rem;
    }

    .know {
      h3 {
        color: $nexgen_white;

        .title_bg {
          background-color: rgba($nexgen_primary_green, 0.2);
        }
      }
    }
  }
}
</style>