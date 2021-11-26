<template>
  <div class="services">
    <div class="container">
      <p class="section_title">Our business areas</p>
      <h3>Excellence in <span class="title_bg">Services</span></h3>
      <div class="d_flex">
        <p>
          We are leaders in providing consultancy services with a set of
          cutting-edge technologies and a team of experienced and renowed
          professionals. These are some options that you can hire.
        </p>
        <div class="btn_green">See all</div>
      </div>

      <div class="cards">
        <div class="d_flex">
          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/audit.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h5>Audit & Assurance</h5>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->

          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/financial.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h5>Financial Advisory</h5>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->

          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/analytics.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h5>Analytics and M&A</h5>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->
        </div>

        <div class="d_flex">
          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/middle.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h5>Middle Marketing</h5>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->

          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/legal.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h5>Legal Consulting</h5>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
          </div>
          <!-- /.card -->

          <div class="card col_3">
            <div class="card_header d_flex">
              <img src="../assets/img/risk.png" />
              <font-awesome-icon
                :icon="['fas', 'arrow-right']"
                class="icon arrow_right"
              />
            </div>
            <h5>Regulatory Risk</h5>
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
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.services {
  background-color: $nexgen_light_green;
  padding: 120px 0;
  color: $nexgen_grey;
  font-weight: 300;

  .container {
    h3 {
      color: $nexgen_primary_blue;
    }

    .title_bg {
      color: $nexgen_primary_green;
      background-color: rgba($nexgen_primary_green, 0.15);
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
          color: $nexgen_primary_green;

          &.arrow_right {
            transition: 0.3s linear;
            font-size: 1.5rem;
            color: rgba($nexgen_primary_green, 0.5);
            cursor: pointer;
          }

          &.arrow_right:hover {
            font-size: 2rem;
            color: $nexgen_primary_green;
          }
        }

        h5 {
          color: $nexgen_primary_blue;
          margin: 1.3rem 0;
        }
      }
    }
  }
}
</style>