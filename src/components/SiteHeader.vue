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

    <div class="bottom_header">
      <div class="navbar container d_flex">
        <div class="logo">
          <span class="logo_bg">Nex</span>
          <span>gen</span>
        </div>
        <div class="menu">
          <ul>
            <li><a href="">home</a></li>
            <li><a href="">about</a></li>
            <li><a href="">services</a></li>
            <li><a href="">process</a></li>
            <li><a href="">team</a></li>
            <li><a href="">blog</a></li>
            <li class="btn_green">get in touch</li>
          </ul>
        </div>
      </div>
      <!-- /.navbar -->

      <div class="consulting">
        <p class="fusions">Fusions & acquisitions</p>
        <h2>Insurance Consulting</h2>
        <div class="d_flex">
          <div class="box">Name</div>
          <div class="box">Email</div>
        </div>
        <div class="d_flex">
          <div class="box">Phone</div>
          <div class="box d_flex">
            More Info
            <font-awesome-icon :icon="['fas', 'chevron-down']" class="icon" />
          </div>
        </div>
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
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

header {
  background-image: url(../assets/img/bg-6.jpg);

  .top_header {
    background-color: $nexgen_dark_blue;
    color: $nexgen_text_header;
    font-size: 0.9rem;
    font-weight: 300;
    padding: 0.9rem 0;

    .container {
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

  .bottom_header {
    .navbar {
      text-transform: uppercase;
      padding: 2rem 0;

      .logo {
        font-family: "Montserrat", sans-serif;
        font-size: 1.2rem;
        letter-spacing: 0.35rem;
        color: $nexgen_text_dark;

        .logo_bg {
          background-color: #c0dadc;
          padding: 0.8rem 0 0.8rem 1.5rem;
          border-radius: 50px 0 0 50px;
          color: #0daaaa;
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
          color: $nexgen_text_dark;
        }
      }
    }

    .consulting {
      width: 50%;
      margin-left: auto;
      margin-top: 150px;
      padding: 0 6rem 220px 3rem;

      .fusions {
        font-size: 1.1rem;
        font-weight: 500;
        text-transform: uppercase;
        color: #0daaaa;
      }

      .d_flex {
        justify-content: flex-start;

        .box {
          background-color: #cdd1d3;
          padding: 0.8rem;
          border-radius: 5px;
          width: 245px;
          margin: 0 1rem 1rem 0;
          color: #8e98a2;
        }
      }

      .box.d_flex {
        justify-content: space-between;
      }

      .btn_green {
        margin-right: 1rem;
      }
    }
  }
}
</style>