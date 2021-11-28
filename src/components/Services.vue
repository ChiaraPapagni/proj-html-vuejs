<template>
  <div class="services">
    <div class="container">
      <p class="section_title">{{ sectionTitle }}</p>
      <h2>
        {{ title.notMarked }} <span class="title_bg">{{ title.marked }}</span>
      </h2>
      <div class="d_flex">
        <p>
          {{ description }}
        </p>
        <div class="btn">See all</div>
      </div>

      <div class="cards">
        <div class="d_flex">
          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/service-1.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h4>Audit & Assurance</h4>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->

          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/service-2.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h4>Financial Advisory</h4>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->

          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/service-3.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h4>Analytics and M&A</h4>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->
        </div>

        <div class="d_flex">
          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/service-4.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h4>Middle Marketing</h4>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->

          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/service-5.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h4>Legal Consulting</h4>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->

          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/service-6.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h4>Regulatory Risk</h4>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->
        </div>
      </div>
      <!-- /.cards -->
    </div>
  </div>
  <!-- /.services -->
</template>

<script>
export default {
  data() {
    return {
      sectionTitle: "Our business areas",
      title: {
        marked: "Services",
        notMarked: "Excellence in",
      },
      description: `We are leaders in providing consultancy services with a set of
          cutting-edge technologies and a team of experienced and renowed
          professionals. These are some options that you can hire.`,
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.services {
  background-color: $nexgen_light_green;
  padding: 130px 0;
  color: $nexgen_grey;
  font-weight: 300;

  .container {
    h2 {
      color: $nexgen_secondary_color;
    }

    .title_bg {
      color: $nexgen_primary_color;
      background-color: rgba($nexgen_primary_color, 0.15);
    }

    .d_flex > p {
      width: 75%;
    }

    .cards {
      margin-top: 3rem;

      & > .d_flex {
        gap: 2rem;
        margin-bottom: 2rem;
      }

      .card {
        transition: 0.3s linear;
        background-color: $nexgen_white;
        border-radius: 10px;
        padding: 3rem;

        &:hover {
          transform: translateY(-7.5px);
        }
        .icon {
          color: $nexgen_primary_color;

          &.arrow_right {
            transition: 0.3s linear;
            font-size: 1.5rem;
            color: rgba($nexgen_primary_color, 0.5);
            cursor: pointer;
          }

          &.arrow_right:hover {
            font-size: 2rem;
            color: $nexgen_primary_color;
          }
        }

        h4 {
          color: $nexgen_secondary_color;
          margin: 1.3rem 0;
        }
      }
    }
  }
}
</style>