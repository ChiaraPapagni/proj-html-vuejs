<template>
  <footer id="site_footer">
    <div class="top_footer">
      <div class="container d_flex">
        <div class="card contacts">
          <div class="logo">
            <span class="logo_bg">Nex</span>
            <span>gen</span>
          </div>
          <!-- /.logo -->
          <p class="info">
            A Functional HTML Template for Corporate & Business.
          </p>
          <p class="contact">
            <font-awesome-icon :icon="['fas', 'phone-alt']" class="icon" />
            <span>{{ phone }}</span>
          </p>
          <p class="contact">
            <font-awesome-icon :icon="['fas', 'envelope']" class="icon" />
            <span>{{ email }}</span>
          </p>
          <p class="contact">
            <font-awesome-icon :icon="['fas', 'map-marker-alt']" class="icon" />
            <span>{{ address }}</span>
          </p>
          <div class="btn_outline">get in touch</div>
        </div>
        <!-- /.contacts -->

        <div class="card link" v-for="(section, i) in footerLinks" :key="i">
          <h4>{{ capitalize(section.title) }}</h4>
          <ul>
            <li v-for="(link, i) in section.links" :key="i">
              <a href="">
                <font-awesome-icon
                  :icon="['fas', 'chevron-right']"
                  class="list_icon"
                />
                <span>{{ link }}</span>
              </a>
            </li>
          </ul>
        </div>
        <!-- /.card -->
      </div>
    </div>
    <!-- /.top_footer -->

    <div class="bottom_footer">
      <div class="container d_flex">
        <p>Enjoy the low price. We are tracking any intention of piracy.</p>
        <p>© 2020 NEXGEN is Proudly Powered by <span>Codings</span>.</p>
      </div>
      <div id="back_to_top" class="arrow_top" v-show="scY > 300" @click="up">
        <font-awesome-icon :icon="['fas', 'arrow-up']" class="icon" />
      </div>
    </div>
    <!-- /.bottom_footer -->
  </footer>
  <!-- /#site_footer -->
</template>

<script>
export default {
  props: {
    phone: String,
    email: String,
    address: String,
  },
  data() {
    return {
      footerLinks: [
        {
          title: "about",
          links: [
            "The Company",
            "Institutional",
            "Social & Events",
            "Innovation",
            "Environment",
            "Technology",
          ],
        },
        {
          title: "services",
          links: [
            "Audit & Assurance",
            "Financial Advisory",
            "Analytics M&A",
            "Middle Marketing",
            "Legal Consulting",
            "Regulatory Risk",
          ],
        },
        {
          title: "support",
          links: [
            "Responsability",
            "Trem of Use",
            "About Cookies",
            "Privacy Policy",
            "Accessibility",
            "Information",
          ],
        },
      ],
      scY: 0,
    };
  },
  methods: {
    capitalize(string) {
      return string.charAt(0).toUpperCase() + string.slice(1);
    },
    scroll() {
      this.scY = window.scrollY;
    },
    up() {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
  },
  mounted() {
    window.addEventListener("scroll", this.scroll);
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

footer {
  color: $nexgen_light_grey_text;

  .top_footer {
    background-color: $nexgen_primary_dark;
    padding: 130px 0 140px 0;
    font-weight: 300;

    .container {
      gap: 2rem;

      .card {
        width: calc(100% / 4);
        height: 325px;
      }

      .contacts {
        .logo {
          font-size: 1.5rem;
          font-weight: 700;
          text-transform: uppercase;
          letter-spacing: 0.35rem;
          margin: 1rem 0 2rem 0;

          .logo_bg {
            background-color: rgba($nexgen_primary_color, 0.2);
            padding: 0.7rem 0 0.7rem 1.8rem;
            border-radius: 50px 0 0 50px;
            color: $nexgen_primary_color;
            margin-right: 0.2rem;
          }
        }

        .info {
          margin: 1.5rem 0;
        }

        p {
          margin-bottom: 1rem;

          span {
            margin-left: 0.5rem;
          }
        }

        .btn_outline {
          margin-top: 0.7rem;
          color: $nexgen_white;
        }

        .contact {
          transition: 0.1s linear;
          cursor: pointer;

          &:hover {
            color: $nexgen_primary_color;
          }
        }
      }

      .link {
        transition: 0.3s linear;
        background-color: $nexgen_dark_grey;
        border-radius: 10px;
        padding: 3rem;

        &:hover {
          transform: translateY(-7.5px);
        }

        h4 {
          color: #f9f9f9;
          margin-bottom: 1rem;
        }

        ul {
          list-style: none;
          padding: 0;
          line-height: 2rem;

          li > a {
            transition: 0.1s linear;
            color: $nexgen_light_grey_text;
            text-decoration: none;

            span {
              margin-left: 0.5rem;
            }

            &:hover {
              color: $nexgen_primary_color;
            }
          }
        }
      }
    }
  }

  .bottom_footer {
    background-color: $nexgen_black;
    padding: 2rem 0;

    p {
      font-size: 0.9rem;
      font-weight: 300;

      & > span {
        color: $nexgen_primary_color;
        cursor: pointer;
      }
    }

    .arrow_top {
      position: fixed;
      z-index: 10;
      right: 1.5rem;
      bottom: 1.5rem;
      width: 50px;
      height: 50px;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #f1f1f1;
      box-shadow: 0 3px 5px rgba($nexgen_black, 15%),
        0 3px 5px rgba($nexgen_black, 25%);
      border-radius: 50%;
      font-size: 1.5rem;
      color: $nexgen_primary_color;
      cursor: pointer;
    }

    .arrow_top:hover {
      box-shadow: 0 15px 25px rgba($nexgen_black, 25%),
        0 10px 10px rgba($nexgen_black, 25%);
    }
  }
}
</style>