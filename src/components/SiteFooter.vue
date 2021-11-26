<template>
  <footer id="site_footer">
    <div class="top_footer">
      <div class="container">{{ address }}</div>
    </div>
    <!-- /.top_footer -->

    <div class="bottom_footer">
      <div class="container d_flex">
        <p>Enjoy the low price. We are tracking any intention of piracy.</p>
        <p>© 2020 NEXGEN is Proudly Powered by <span>Codings</span>.</p>
      </div>
    </div>
    <!-- /.bottom_footer -->
  </footer>
  <!-- /#site_footer -->
</template>

<script>
export default {
  props: {
    address: String,
  },
  data() {
    return {
      about: [
        "The Company",
        "Institutional",
        "Social & Events",
        "Innovation",
        "Environment",
        "Technology",
      ],
      services: [
        "Audit & Assurance",
        "Financial Advisory",
        "Analytics M&A",
        "Middle Marketing",
        "Legal Consulting",
        "Regulatory Risk",
      ],
      support: [
        "Responsability",
        "Trem of Use",
        "About Cookies",
        "Privacy Policy",
        "Accessibility",
        "Information",
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

footer {
  .top_footer {
    background-color: $nexgen_bg_dark;
  }

  .bottom_footer {
    background-color: #0d0d11;
    padding: 2rem 0;

    p {
      font-size: 0.9rem;
      font-weight: 300;
      color: #ccc;

      & > span {
        color: $nexgen_primary_green;
      }
    }
  }
}
</style>