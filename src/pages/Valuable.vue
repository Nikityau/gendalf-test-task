<script setup>
import {nanoid} from "nanoid";
import {Swiper, SwiperSlide} from 'swiper/vue';
import {Autoplay} from "swiper/modules";
import ValueCard from "@/entity/ValueCard.vue";

import 'swiper/css';

import Image from '@/assets/value-image.png'

const img = Image

const data = [
  {
    id: nanoid(),
    title: 'Быть командой',
    description: 'Готовность вносить вклад в общие цели команды и достигать их.',
    image: img
  },
  {
    id: nanoid(),
    title: 'Быть командой',
    description: 'Готовность вносить вклад в общие цели команды и достигать их.',
    image: img
  },
  {
    id: nanoid(),
    title: 'Быть командой',
    description: 'Готовность вносить вклад в общие цели команды и достигать их.',
    image: img
  },
  {
    id: nanoid(),
    title: 'Быть командой',
    description: 'Готовность вносить вклад в общие цели команды и достигать их.',
    image: img
  },
  {
    id: nanoid(),
    title: 'Быть командой',
    description: 'Готовность вносить вклад в общие цели команды и достигать их.',
    image: img
  },
  {
    id: nanoid(),
    title: 'Быть командой',
    description: 'Готовность вносить вклад в общие цели команды и достигать их.',
    image: img
  },
  {
    id: nanoid(),
    title: 'Быть командой',
    description: 'Готовность вносить вклад в общие цели команды и достигать их.',
    image: img
  },
]
</script>

<template>
  <article class="valuable">
    <div class="valuable__header">
      <h3>Наши ценности скажут о нас больше:</h3>
    </div>
    <swiper
        :slides-per-view="'auto'"
        :modules="[Autoplay]"

        :loop="true"
    >
      <swiper-slide
          v-for="(item, index) in data"
          :key="item.id"
      >
        <ValueCard
            :title="item.title"
            :description="item.description"
            :image="item.image"
            :number="index + 1"
        />
      </swiper-slide>
    </swiper>
  </article>
</template>
<style>
.valuable {
  padding: 36px 0 70px;

  background: #E9E9E9;

  .swiper {
    .swiper-slide {
      width: 30%;
    }
  }

  @media screen and (max-width: 970px){
    .swiper {
      .swiper-slide {
        width: 47%;
      }
    }
  }
  @media screen and (max-width: 620px){
    .swiper {
      .swiper-slide {
        width: 60%;
      }
    }
  }
  @media screen and (max-width: 500px){
    .swiper {
      .swiper-slide {
        width: 75%;
      }
    }
  }

  .valuable__header {
    padding: 0 var(--side-padding);

    margin-bottom: 40px;

    h3 {
      font-family: Open Sans, sans-serif;
      font-size: 36px;
      font-weight: 300;

      color: var(--color-blue-l)
    }
  }
}
</style>