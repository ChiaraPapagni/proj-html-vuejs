<template>
  <header id="site_header">
    <div class="top_header">
      <div class="container d_flex">
        <div class="left d_flex">
          <font-awesome-icon :icon="['fas', 'clock']" class="icon" />
          <p>Open Hours: Mon - Sat - 9.00 - 18.00</p>
        </div>
        <!-- /.left -->
        <div class="right d_flex">
          <p class="phone d_flex">
            <font-awesome-icon :icon="['fas', 'phone-alt']" class="icon" />
            +1 (305) 1234-5678
          </p>
          <p class="email d_flex">
            <font-awesome-icon :icon="['fas', 'envelope']" class="icon" />
            hello@example.com
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
  </header>
  <!-- /#site_header -->
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.top_header {
  background-color: $nexgen_dark_blue;
  color: $nexgen_text_header;
  font-size: 0.9rem;
  font-weight: 300;
  padding: 0.9rem 0;

  .container {
    justify-content: space-between;

    .left > p {
      margin-left: 0.5rem;
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
    }
  }
}
</style>