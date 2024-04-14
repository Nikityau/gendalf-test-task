<script setup>
import {nanoid} from 'nanoid'

const navData = [
  {
    id: nanoid(),
    link: '#',
    text: 'Профориентация'
  },
  {
    id: nanoid(),
    link: '#',
    text: 'Выбрать вакансию'
  },
  {
    id: nanoid(),
    link: '#',
    text: 'Карьера в ГЭНДАЛЬФ'
  },
  {
    id: nanoid(),
    link: '#',
    text: 'Стажерство'
  },
  {
    id: nanoid(),
    link: '#',
    text: 'Отзывы'
  },
]
</script>

<template>
  <nav class="nav">
    <a
        v-for="(nav) in navData"
        :key="nav.id"
        :href="nav.link"
    >
      {{ nav.text }}
    </a>
  </nav>
</template>

<style>
.nav {
  display: flex;
  align-items: center;
  gap: 39px;

  a {
    font-family: Open Sans, sans-serif;
    font-size: 18px;
    font-weight: 400;

    color: #fff;
  }
}
</style>