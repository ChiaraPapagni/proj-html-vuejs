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
      </div>
      <div class="research">
        <h5>Because market research is part of the business plan</h5>
      </div>
      <div class="home_work">
        <h5>Working from home is now a trend</h5>
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
  color: #66737b;
  font-weight: 300;

  h3 {
    color: $nexgen_text_dark;

    .title_bg {
      background-color: #daeced;
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
      padding: 2rem;

      h5 {
        position: absolute;
        left: 0rem;
        bottom: 2rem;
        color: white;
        text-align: center;
        line-height: 1.8rem;
        padding: 0 2rem;
      }
    }

    .creativity {
      background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
        url("../assets/img/news-1.jpg");
      background-size: contain;
      position: relative;
    }

    .research {
      background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
        url("../assets/img/news-2.jpg");
      background-size: contain;
      position: relative;
    }

    .home_work {
      background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
        url("../assets/img/news-3.jpg");
      background-size: contain;
      position: relative;
    }
  }
}
</style>