<template id="blog">
  <div class="news container">
    <p class="section_title">{{ sectionTitle }}</p>
    <h3>
      {{ title.notMarked }} <span class="title_bg">{{ title.marked }}</span>
    </h3>
    <div class="d_flex">
      <p>
        {{ description }}
      </p>
      <div class="btn_green">see all</div>
    </div>

    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide class="swiper-slide">
        <div class="card">
          <img src="../assets/img/news-1.jpg" />
          <div class="info">
            <div class="card_header d_flex">
              <p>
                <font-awesome-icon :icon="['far', 'user']" class="icon" />
                <span>Andrea Miller</span>
              </p>
              <p>
                <font-awesome-icon
                  :icon="['far', 'clock']"
                  class="icon clock"
                />
                <span>2 Days Ago</span>
              </p>
            </div>
            <h5>Increasing creativity is possible for everyone</h5>
            <p class="desc">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            </p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <div class="card">
          <img src="../assets/img/news-2.jpg" />
          <div class="info">
            <div class="card_header d_flex">
              <p>
                <font-awesome-icon :icon="['far', 'user']" class="icon" />
                <span>John Smith</span>
              </p>
              <p>
                <font-awesome-icon
                  :icon="['far', 'clock']"
                  class="icon clock"
                />
                <span>9 Days Ago</span>
              </p>
            </div>
            <h5>Because market research is part of the business plan</h5>
            <p class="desc">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            </p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <div class="card">
          <img src="../assets/img/news-3.jpg" />
          <div class="info">
            <div class="card_header d_flex">
              <p>
                <font-awesome-icon :icon="['far', 'user']" class="icon" />
                <span>Andrea Miller</span>
              </p>
              <p>
                <font-awesome-icon
                  :icon="['far', 'clock']"
                  class="icon clock"
                />
                <span>16 Days Ago</span>
              </p>
            </div>
            <h5>Working from home is now a trend</h5>
            <p class="desc">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            </p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <div class="card">
          <img src="../assets/img/news-4.jpg" />
          <div class="info">
            <div class="card_header d_flex">
              <p>
                <font-awesome-icon :icon="['far', 'user']" class="icon" />
                <span>John Smith</span>
              </p>
              <p>
                <font-awesome-icon
                  :icon="['far', 'clock']"
                  class="icon clock"
                />
                <span>23 Days Ago</span>
              </p>
            </div>
            <h5>Tips for having a goog relationship at work</h5>
            <p class="desc">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            </p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="swiper-slide">
        <div class="card">
          <img src="../assets/img/news-5.jpg" />
          <div class="info">
            <div class="card_header d_flex">
              <p>
                <font-awesome-icon :icon="['far', 'user']" class="icon" />
                <span>David Cooper</span>
              </p>
              <p>
                <font-awesome-icon
                  :icon="['far', 'clock']"
                  class="icon clock"
                />
                <span>30 Days Ago</span>
              </p>
            </div>
            <h5>
              David Cooper tells about the opening of the new office in
              Baltimore
            </h5>
            <p class="desc">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            </p>
          </div>
        </div>
      </swiper-slide>
    </swiper>

    <!-- <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide class="swiper-slide" v-for="(item, i) in news" :key="i">
        <div class="card">
          <img :src="item.poster" />

          <div class="info">
            <div class="card_header d_flex">
              <p>
                <font-awesome-icon :icon="['far', 'user']" class="icon" />
                <span>{{ item.name }}</span>
              </p>
              <p>
                <font-awesome-icon
                  :icon="['far', 'clock']"
                  class="icon clock"
                />
                <span>{{ item.date }}</span>
              </p>
            </div>
            <h5>{{ item.title }}</h5>
            <p class="desc">
              {{ item.desc }}
            </p>
          </div>
        </div>
      </swiper-slide>
    </swiper> -->
  </div>
  <!-- /.news -->
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      sectionTitle: "our editorial content",
      title: {
        marked: "News",
        notMarked: "Latest",
      },
      description: `Every week we publish content about what is best in the business world.`,
      news: [
        {
          name: "Andrea Miller",
          date: "2 Days Ago",
          title: "Increasing creativity is possible for everyone",
          poster: "news-1",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          name: "John Smith",
          date: "9 Days Ago",
          title: "Because market research is part of the business plan",
          poster: "../assets/img/news-2.jpg",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          name: "Andrea Miller",
          date: "16 Days Ago",
          title: "Working from home is now a trend",
          poster: "../assets/img/news-3.jpg",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          name: "John Smith",
          date: "23 Days Ago",
          title: "Tips for having a goog relationship at work",
          poster: "../assets/img/news-4.jpg",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          name: "David Cooper",
          date: "30 Days Ago",
          title:
            "David Cooper tells about the opening of the new office in Baltimore",
          poster: "../assets/img/news-5.jpg",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
      ],
      swiperOptions: {
        slidesPerView: 3,
        spaceBetween: 30,
        loop: true,
      },
    };
  },
};
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

  .card {
    width: 350px;
    height: 350px;
    margin-top: 3rem;
    overflow: hidden;
    border-radius: 10px;
    position: relative;
    text-align: center;
    color: $nexgen_white;
    cursor: ew-resize;

    img {
      transition: 0.3s ease;
      width: 350px;
      height: 350px;
      object-fit: contain;
      border-radius: 10px;
      filter: brightness(0.6);
    }

    .info {
      padding: 0 2rem;

      .card_header {
        transition: 0.3s ease;
        position: absolute;
        left: 0rem;
        top: -3rem;
        padding: 0 2.2rem;

        .icon {
          margin-right: 0.5rem;

          &.clock {
            margin-left: 1.5rem;
          }
        }
      }

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

      .desc {
        transition: 0.3s ease;
        position: absolute;
        left: 0rem;
        bottom: -3rem;
        padding: 0 2rem;
      }
    }

    &:hover img {
      transform: scale(1.1);
      object-fit: contain;
      object-position: center;
      filter: blur(1px) brightness(0.3);
    }

    &:hover .card_header {
      top: 3rem;
    }
    &:hover h5 {
      bottom: 7.5rem;
    }
    &:hover .desc {
      bottom: 3rem;
    }
  }
}
</style>