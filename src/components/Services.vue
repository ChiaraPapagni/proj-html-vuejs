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
              <font-awesome-icon :icon="['far', 'edit']" class="icon" />
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
              <font-awesome-icon :icon="['far', 'edit']" class="icon" />
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
              <font-awesome-icon :icon="['far', 'edit']" class="icon" />
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
              <font-awesome-icon :icon="['far', 'edit']" class="icon" />
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
              <font-awesome-icon :icon="['far', 'edit']" class="icon" />
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
              <font-awesome-icon :icon="['far', 'edit']" class="icon" />
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
  background-color: #eef4ed;
  padding: 120px 0;
  color: #7e878c;
  font-weight: 300;

  .container {
    h3 {
      color: $nexgen_text_dark;
    }

    .title_bg {
      color: $nexgen_primary_green;
      background-color: #cce3de;
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
        background-color: white;
        border-radius: 10px;
        padding: 3rem;

        .icon {
          color: $nexgen_primary_green;

          &.arrow_right {
            font-size: 1.5rem;
            color: #82c1c1;
          }
        }

        h5 {
          color: $nexgen_dark_blue;
          margin: 1rem 0;
        }
      }
    }
  }
}
</style>