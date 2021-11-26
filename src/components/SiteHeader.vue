<template>
  <header id="site_header">
    <div class="top_header">
      <div class="container d_flex">
        <div class="left d_flex">
          <font-awesome-icon :icon="['fas', 'clock']" class="icon" />
          <p>Open Hours: {{ openHours.days }} - {{ openHours.hours }}</p>
        </div>
        <!-- /.left -->
        <div class="right d_flex">
          <p class="phone d_flex">
            <font-awesome-icon :icon="['fas', 'phone-alt']" class="icon" />
            {{ phone }}
          </p>
          <p class="email d_flex">
            <font-awesome-icon :icon="['fas', 'envelope']" class="icon" />
            {{ email }}
          </p>
          <p>
            <font-awesome-icon
              :icon="['fab', 'facebook-f']"
              class="social_icon"
            />
            <font-awesome-icon :icon="['fab', 'twitter']" class="social_icon" />
            <font-awesome-icon
              :icon="['fab', 'linkedin-in']"
              class="social_icon"
            />
          </p>
        </div>
        <!-- /.right -->
      </div>
    </div>
    <!-- /.top_header -->

    <div class="bottom_header">
      <div class="navbar container d_flex">
        <div class="logo">
          <span class="logo_bg">Nex</span>
          <span>gen</span>
        </div>
        <div class="menu">
          <ul>
            <li v-for="(page, i) in pages" :key="i">
              <a href="" class="underline">
                <span>{{ page.name }}</span>
              </a>
            </li>
            <li class="btn_green">get in touch</li>
          </ul>
        </div>
      </div>
      <!-- /.navbar -->

      <div class="consulting">
        <p class="fusions">Fusions & acquisitions</p>
        <h2>Insurance Consulting</h2>
        <div class="form d_flex">
          <input type="text" placeholder="Name" class="input" />
          <input type="text" placeholder="Email" class="input" />
        </div>
        <div class="form d_flex">
          <input type="tel" placeholder="Phone" class="input" />
          <select name="info" class="input">
            <option value selected disabled>More Info</option>
            <option>Audit & Assurance</option>
            <option>Financial Advisory</option>
            <option>Analytics and M&A</option>
            <option>Middle Marketing</option>
            <option>Legal Consulting</option>
            <option>Regulatory Risk</option>
            <option>Other</option>
          </select>
        </div>
        <!-- /.form -->

        <div class="btn d_flex">
          <div class="btn_green">get in touch</div>
          <div class="btn_green_outline">read more</div>
        </div>
      </div>
      <!-- /.consulting -->
    </div>
    <!-- /.bottom_header -->
  </header>
  <!-- /#site_header -->
</template>

<script>
export default {
  props: {
    phone: String,
    email: String,
    openHours: Object,
  },
  data() {
    return {
      pages: [
        {
          name: "home",
        },
        {
          name: "about",
        },
        {
          name: "services",
        },
        {
          name: "process",
        },
        {
          name: "team",
        },
        {
          name: "blog",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

header {
  background-image: url(../assets/img/bg-6.jpg);
  background-position-y: center;

  .top_header {
    background-color: $nexgen_primary_blue;
    color: $nexgen_light_grey_text;
    font-size: 0.9rem;
    font-weight: 300;
    padding: 0.9rem 0;

    .container {
      .left {
        transition: 0.1s linear;

        p {
          margin-left: 0.5rem;
        }

        &:hover {
          color: $nexgen_primary_green;
          cursor: pointer;
        }
      }

      .right {
        .phone {
          margin-right: 2rem;
        }

        .icon {
          margin-right: 0.5rem;
        }

        .social_icon {
          margin-left: 2rem;
        }

        .phone,
        .email,
        .social_icon {
          transition: 0.1s linear;
          cursor: pointer;

          &:hover {
            color: $nexgen_primary_green;
          }
        }
      }
    }
  }

  .bottom_header {
    .navbar {
      text-transform: uppercase;
      padding: 2rem 0;

      .logo {
        font-family: "Montserrat", sans-serif;
        font-size: 1.2rem;
        letter-spacing: 0.35rem;
        color: $nexgen_primary_blue;

        .logo_bg {
          background-color: rgba($nexgen_primary_green, 0.15);
          padding: 0.8rem 0 0.8rem 1.5rem;
          border-radius: 50px 0 0 50px;
          color: $nexgen_primary_green;
          margin-right: 0.2rem;
        }
      }

      ul > li {
        display: inline;
        list-style: none;
        margin-left: 2rem;

        a {
          font-size: 1.1rem;
          text-decoration: none;
          color: $nexgen_primary_blue;

          &:hover {
            color: $nexgen_primary_green;
          }
        }

        .underline {
          position: relative;
        }

        .underline::before {
          content: "";
          position: absolute;
          top: 24px;
          bottom: 0;
          right: 0;
          width: 0;
          height: 2px;
          background-color: $nexgen_primary_green;
          transition: width 0.6s cubic-bezier(0.25, 1, 0.5, 1);
        }

        @media (hover: hover) and (pointer: fine) {
          .underline:hover::before {
            left: 0;
            right: auto;
            width: 100%;
          }
        }
      }
    }

    .consulting {
      width: 50%;
      margin-left: auto;
      margin-top: 150px;
      padding: 0 6rem 200px 3rem;

      .fusions {
        font-size: 1.1rem;
        font-weight: 500;
        text-transform: uppercase;
        color: #00a6a6;
      }

      .form {
        &.d_flex {
          justify-content: flex-start;
          gap: 1rem;
        }

        .input {
          width: 245px;
          background-color: rgba($nexgen_black, 0.1);
        }

        .more_info {
          font-family: "Arial";
          color: #757575;
        }
      }

      .btn.d_flex {
        justify-content: flex-start;
      }

      .btn_green {
        margin-right: 1rem;
      }
    }
  }
}
</style>