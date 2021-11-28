<template id="blog">
  <div class="news container">
    <p class="section_title">{{ sectionTitle }}</p>
    <h2>
      {{ title.notMarked }} <span class="title_bg">{{ title.marked }}</span>
    </h2>
    <div class="d_flex">
      <p>
        {{ description }}
      </p>
      <div class="btn">see all</div>
    </div>

    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide class="swiper-slide" v-for="(item, i) in news" :key="i">
        <div class="card">
          <img :src="item.poster.url" />

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
            <h4>{{ item.title }}</h4>
            <p class="desc">
              {{ item.desc }}
            </p>
          </div>
        </div>
      </swiper-slide>
    </swiper>
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
          poster: { url: require("../assets/img/news-1.jpg") },
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          name: "John Smith",
          date: "9 Days Ago",
          title: "Because market research is part of the business plan",
          poster: { url: require("../assets/img/news-2.jpg") },
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          name: "Andrea Miller",
          date: "16 Days Ago",
          title: "Working from home is now a trend",
          poster: { url: require("../assets/img/news-3.jpg") },
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          name: "John Smith",
          date: "23 Days Ago",
          title: "Tips for having a goog relationship at work",
          poster: { url: require("../assets/img/news-4.jpg") },
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          name: "David Cooper",
          date: "30 Days Ago",
          title:
            "David Cooper tells about the opening of the new office in Baltimore",
          poster: { url: require("../assets/img/news-5.jpg") },
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
  padding: 130px 0;
  color: $nexgen_grey;
  font-weight: 300;

  h2 {
    color: $nexgen_secondary_color;
    margin: 0.5rem 0;

    .title_bg {
      background-color: rgba($nexgen_primary_color, 0.15);
      color: $nexgen_primary_color;
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

      h4 {
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
    &:hover h4 {
      bottom: 7.5rem;
    }
    &:hover .desc {
      bottom: 3rem;
    }
  }
}
</style>