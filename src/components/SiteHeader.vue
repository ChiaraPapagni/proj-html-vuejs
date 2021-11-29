<template>
  <header id="home">
    <div class="top_header">
      <div class="container d_flex">
        <div class="left d_flex">
          <font-awesome-icon :icon="['fas', 'clock']" class="icon" />
          Open Hours: {{ openHours.days }} - {{ openHours.hours }}
        </div>
        <!-- /.left -->
        <div class="right d_flex">
          <span class="phone d_flex">
            <font-awesome-icon :icon="['fas', 'phone-alt']" class="icon" />
            {{ phone }}
          </span>
          <span class="email d_flex">
            <font-awesome-icon :icon="['fas', 'envelope']" class="icon" />
            {{ email }}
          </span>
          <span>
            <font-awesome-icon
              :icon="['fab', 'facebook-f']"
              class="social_icon"
            />
            <font-awesome-icon :icon="['fab', 'twitter']" class="social_icon" />
            <font-awesome-icon
              :icon="['fab', 'linkedin-in']"
              class="social_icon"
            />
          </span>
        </div>
        <!-- /.right -->
      </div>
    </div>
    <!-- /.top_header -->

    <div class="bottom_header">
      <div class="navbar" :class="{ sticky: scroll }">
        <div class="container d_flex">
          <div class="logo">
            <span class="logo_bg">Nex</span>
            <span>gen</span>
          </div>
          <div class="menu">
            <ul>
              <li v-for="(page, i) in pages" :key="i">
                <a :href="'#' + page.name" class="underline">
                  <span>{{ page.name }}</span>
                </a>
              </li>
              <li class="btn">get in touch</li>
            </ul>
          </div>
        </div>
      </div>
      <!-- /.navbar -->

      <div class="consulting">
        <p class="fusions">{{ insuranceConsulting.info }}</p>
        <h1>{{ insuranceConsulting.title }}</h1>
        <div class="form d_flex">
          <input type="text" placeholder="Name" class="input" />
          <input type="text" placeholder="Email" class="input" />
        </div>
        <div class="form d_flex">
          <input type="tel" placeholder="Phone" class="input" />
          <select name="info" class="input">
            <option value selected disabled>More Info</option>
            <option v-for="(info, i) in insuranceConsulting.moreInfo" :key="i">
              {{ info }}
            </option>
          </select>
        </div>
        <!-- /.form -->

        <div class="btn_group d_flex">
          <div class="btn">get in touch</div>
          <div class="btn_outline">read more</div>
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
      insuranceConsulting: {
        info: "Fusions & acquisitions",
        title: "Insurance Consulting",
        moreInfo: [
          "Audit & Assurance",
          "Financial Advisory",
          "Analytics and M&A",
          "Middle Marketing",
          "Legal Consulting",
          "Regulatory Risk",
          "Other",
        ],
      },
      scroll: false,
    };
  },
  methods: {
    handleScroll() {
      if (window.scrollY > 0) {
        this.scroll = true;
      } else {
        this.scroll = false;
      }
    },
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

header {
  background-image: url(../assets/img/bg-6.jpg);
  background-position-y: center;
  background-attachment: fixed;

  .top_header {
    background-color: $nexgen_secondary_color;
    color: $nexgen_light_grey_text;
    font-size: 0.9rem;
    padding: 1rem 0;

    .container {
      .left {
        transition: 0.1s linear;

        .icon {
          margin-right: 0.5rem;
        }

        &:hover {
          color: $nexgen_primary_color;
          cursor: pointer;
        }
      }

      .right {
        .phone {
          margin-right: 2.2rem;
        }

        .icon {
          margin-right: 0.5rem;
        }

        .social_icon {
          margin-left: 2.2rem;
        }

        .phone,
        .email,
        .social_icon {
          transition: 0.1s linear;
          cursor: pointer;

          &:hover {
            color: $nexgen_primary_color;
          }
        }
      }
    }
  }

  .bottom_header {
    .navbar {
      transition: 0.2s linear;
      font-size: 1rem;
      font-weight: 500;
      text-transform: uppercase;
      padding: 2rem 0;

      .logo {
        font-size: 1.2rem;
        font-weight: 700;
        letter-spacing: 0.35rem;
        color: $nexgen_secondary_color;

        .logo_bg {
          background-color: rgba($nexgen_primary_color, 0.15);
          padding: 0.7rem 0 0.7rem 1.8rem;
          border-radius: 50px 0 0 50px;
          color: $nexgen_primary_color;
          margin-right: 0.2rem;
        }
      }

      ul > li {
        display: inline;
        list-style: none;
        margin-left: 2rem;

        a {
          text-decoration: none;
          color: $nexgen_secondary_color;

          &:hover {
            color: $nexgen_primary_color;
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
          background-color: $nexgen_primary_color;
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

    .sticky {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: $nexgen_white;
      box-shadow: 0 2px 25px 0 rgba($nexgen_black, 10%);
      padding: 1.2rem 0;
      z-index: 10;
    }

    .consulting {
      width: 50%;
      margin-left: auto;
      margin-top: 150px;
      padding: 0 6rem 250px 3rem;

      .fusions {
        font-size: 1rem;
        font-weight: 600;
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
          font-family: $nexgen_paragraph_font;
        }

        select {
          appearance: none;
          -moz-appearance: none;
          -webkit-appearance: none;
          background-image: url("../assets/img/chevron-down.svg");
          background-repeat: no-repeat;
          background-position-x: calc(100% - 1rem);
          background-position-y: 1.1rem;
          color: $nexgen_grey;

          option {
            color: $nexgen_dark_grey;
          }
        }

        .more_info {
          font-family: "Arial";
        }
      }

      .btn_group.d_flex {
        justify-content: flex-start;
      }

      .btn {
        margin-right: 1rem;
      }
    }
  }
}
</style>