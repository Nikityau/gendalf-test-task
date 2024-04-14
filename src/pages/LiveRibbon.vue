<script setup>
import {nanoid} from "nanoid";
import {Swiper, SwiperSlide} from 'swiper/vue';
import {Navigation} from "swiper/modules";

import 'swiper/css';

import Economic from "@/assets/economic.png"
import LiveCard from "@/entity/LiveCard.vue";

import 'swiper/css/navigation';

const img = Economic

const data = [
  {
    id: nanoid(),
    description: 'Экономим на бумаге и угадываем фильмы: дайджест видео марта 2022 года',
    image: img,
  },
  {
    id: nanoid(),
    description: 'Экономим на бумаге и угадываем фильмы: дайджест видео марта 2022 года',
    image: img,
  },
  {
    id: nanoid(),
    description: 'Экономим на бумаге и угадываем фильмы: дайджест видео марта 2022 года',
    image: img,
  },
  {
    id: nanoid(),
    description: 'Экономим на бумаге и угадываем фильмы: дайджест видео марта 2022 года',
    image: img,
  },
  {
    id: nanoid(),
    description: 'Экономим на бумаге и угадываем фильмы: дайджест видео марта 2022 года',
    image: img,
  },
  {
    id: nanoid(),
    description: 'Экономим на бумаге и угадываем фильмы: дайджест видео марта 2022 года',
    image: img,
  },
  {
    id: nanoid(),
    description: 'Экономим на бумаге и угадываем фильмы: дайджест видео марта 2022 года',
    image: img,
  },
  {
    id: nanoid(),
    description: 'Экономим на бумаге и угадываем фильмы: дайджест видео марта 2022 года',
    image: img,
  },
  {
    id: nanoid(),
    description: 'Экономим на бумаге и угадываем фильмы: дайджест видео марта 2022 года',
    image: img,
  },
]
</script>
<template>
  <article class="live-ribbon">
    <div class="live-ribbon__container">
      <h3>Живая лента</h3>
      <div class="live-ribbon__swiper">
        <swiper
            ref="test"
            :slides-per-view="'auto'"
            :space-between="28"
            :modules="[Navigation]"
            :navigation="true"
        >
          <swiper-slide
              v-for="item in data"
              :key="item.id"
          >
            <LiveCard
                :description="item.description"
                :image="item.image"
            />
          </swiper-slide>
        </swiper>
      </div>
    </div>
  </article>
</template>
<style>
.live-ribbon {
  padding: 33px var(--side-padding) 47px;

  background: #E9E9E9;

  h3 {
    font-family: Open Sans, sans-serif;
    font-size: 36px;
    font-weight: 300;

    color: var(--color-blue-l);
  }

  .live-ribbon__swiper {
    margin-top: 21px;

    display: flex;
    align-items: center;
    gap: 22px;
  }

  .live-ribbon__arrow {
    background: none;
    border: none;
  }

  .swiper {
    .swiper-slide {
      width: 25%;
    }
  }

  @media screen and (max-width: 1200px) {
    .swiper {
      .swiper-slide {
        width: 30%;
      }
    }
  }
  @media screen and (max-width: 900px) {
    .swiper {
      .swiper-slide {
        width: 40%;
      }
    }
  }
  @media screen and (max-width: 650px) {
    .swiper {
      .swiper-slide {
        width: 50%;
      }
    }
  }
  @media screen and (max-width: 550px) {
    .swiper {
      padding: 0 40px;

      .swiper-slide {
        width: 100%;

        .live-card {
          width: 100%;
        }
      }
    }
  }
}
</style>