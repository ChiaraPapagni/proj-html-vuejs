<template>
  <div class="about">
    <div class="container d_flex">
      <div class="col">
        <p class="section_title">{{ sectionTitle }}</p>
        <h2>
          <span class="title_bg">{{ title.marked }}</span>
          {{ title.notMarked }}
        </h2>
        <p>
          {{ description }}
        </p>
        <p>
          {{ information }}
        </p>
      </div>
      <div class="col d_flex">
        <div class="col">
          <h4>
            <font-awesome-icon :icon="['fas', 'medal']" class="icon" />Tradition
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
  <!-- /.about -->
</template>

<script>
export default {
  data() {
    return {
      sectionTitle: "about the network",
      title: {
        marked: "The",
        notMarked: "Company",
      },
      description: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cras iaculis
          diam varius diam ultricies lacina. Mauris lacus tellus, ultrices eu
          volutpat sit amet, finibus a ipsum.`,
      information: `Curabitur convallis, diam a egestas iaculis, neque lorem interdum
          falis, in viverra lacus tortor in leo.`,
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.about {
  background-color: $nexgen_primary_dark;
  padding: 130px 0;
  color: $nexgen_light_grey_text;
  font-weight: 300;

  .container {
    align-items: end;
    gap: 6.5rem;

    h2 {
      color: $nexgen_white;
    }

    .title_bg {
      background-color: rgba($nexgen_primary_color, 0.2);
    }

    p {
      margin: 1rem 0;
    }

    .icon {
      color: $nexgen_primary_color;
      font-size: 1.4rem;
      margin-right: 0.5rem;
    }

    h4 {
      color: $nexgen_white;
    }
  }
}
</style>