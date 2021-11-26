<template>
  <div class="news container">
    <p class="section_title">our editorial content</p>
    <h3>Latest <span class="title_bg">News</span></h3>
    <div class="d_flex">
      <p>
        Every week we publish content about what is best in the business world.
      </p>
      <div class="btn_green">see all</div>
    </div>

    <div class="d_flex image">
      <div class="creativity">
        <h5>Increasing creativity is possible for everyone</h5>
        <div class="wrap">
          <div class="header d_flex">
            <p>
              <font-awesome-icon :icon="['far', 'user']" class="icon" />
              <span>Andrea Miller</span>
            </p>
            <p>
              <font-awesome-icon :icon="['far', 'clock']" class="icon clock" />
              <span>2 Days Ago</span>
            </p>
          </div>
          <h5>Increasing creativity is possible for everyone</h5>
          <p class="desc">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit.
          </p>
        </div>
      </div>

      <div class="research">
        <h5>Because market research is part of the business plan</h5>
        <div class="wrap">
          <div class="header d_flex">
            <p>
              <font-awesome-icon :icon="['far', 'user']" class="icon" />
              <span>John Smith</span>
            </p>
            <p>
              <font-awesome-icon :icon="['far', 'clock']" class="icon clock" />
              <span>9 Days Ago</span>
            </p>
          </div>
          <h5>Because market research is part of the business plan</h5>
          <p class="desc">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit.
          </p>
        </div>
      </div>

      <div class="home_work">
        <h5>Working from home is now a trend</h5>
        <div class="wrap">
          <div class="header d_flex">
            <p>
              <font-awesome-icon :icon="['far', 'user']" class="icon" />
              <span>Andrea Miller</span>
            </p>
            <p>
              <font-awesome-icon :icon="['far', 'clock']" class="icon clock" />
              <span>16 Days Ago</span>
            </p>
          </div>
          <h5>Working from home is now a trend</h5>
          <p class="desc">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit.
          </p>
        </div>
      </div>
    </div>
  </div>
  <!-- /.news -->
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.news {
  padding: 120px 0;
  color: $nexgen_grey;
  font-weight: 300;

  h3 {
    color: $nexgen_primary_blue;

    .title_bg {
      background-color: rgba($nexgen_primary_green, 0.15);
      color: $nexgen_primary_green;
    }
  }

  .image {
    gap: 1rem;
    margin-top: 3rem;

    & > div {
      width: 350px;
      height: 350px;
      border-radius: 10px;

      h5 {
        transition: 0.3s ease;
        position: absolute;
        left: 0rem;
        bottom: 2rem;
        color: $nexgen_white;
        text-align: center;
        line-height: 1.8rem;
        padding: 0 2rem;
      }
    }

    .creativity {
      background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
        url("../assets/img/news-1.jpg");
      background-size: contain;
      position: relative;
      cursor: pointer;

      &:hover .wrap {
        opacity: 1;
      }

      &:hover .header {
        top: 3rem;
      }
      &:hover h5 {
        bottom: 8rem;
      }
      &:hover .desc {
        bottom: 3rem;
      }
    }

    .research {
      background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
        url("../assets/img/news-2.jpg");
      background-size: contain;
      position: relative;
      cursor: pointer;

      &:hover .wrap {
        opacity: 1;
      }

      &:hover .header {
        top: 3rem;
      }

      &:hover h5 {
        bottom: 8rem;
      }
      &:hover .desc {
        bottom: 3rem;
      }
    }

    .home_work {
      background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
        url("../assets/img/news-3.jpg");
      background-size: contain;
      position: relative;
      cursor: pointer;

      &:hover .wrap {
        opacity: 1;
      }

      &:hover .header {
        top: 3rem;
      }
      &:hover h5 {
        bottom: 8rem;
      }
      &:hover .desc {
        bottom: 3rem;
      }
    }

    .wrap {
      position: relative;
      transition: 0.8s ease-in-out;
      width: 100%;
      height: 100%;
      padding: 3rem 2rem;
      background-color: rgba($nexgen_black, $alpha: 0.4);
      border-radius: 10px;
      color: $nexgen_white;
      text-align: center;
      opacity: 0;

      .header {
        transition: 0.3s ease;
        position: absolute;
        left: 0rem;
        top: -10rem;
        padding: 0 2.5rem;

        .icon {
          margin-right: 0.5rem;

          &.clock {
            margin-left: 1.5rem;
          }
        }
      }

      .desc {
        transition: 0.3s ease;
        position: absolute;
        left: 0rem;
        bottom: -5rem;
        padding: 0 2rem;
      }
    }
  }
}
</style>