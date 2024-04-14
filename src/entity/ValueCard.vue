<script setup>

const {
  number,
  description,
  image,
  title
} = defineProps(['number', 'title', 'description', 'image'])
</script>

<template>
<section class="value-card">
  <img :src="image" alt="image">
  <div class="value-card__description">
    <h4>{{ title }}</h4>
    <p>{{ description }}</p>
  </div>
  <div class="value-card__number">
    <span>{{ number }}</span>
  </div>
</section>
</template>

<style>
.value-card {
  position: relative;

  .value-card__description {
    max-width: 300px;

    margin-top: 15px;

    text-align: center;

    font-family: Open Sans, sans-serif;
    font-size: 20px;
    font-weight: 700;

    color: var(--color-gray);
    
    h4 {
      text-decoration: underline;
    }
    p {
      margin-top: 10px;

      font-size: 16px;
      font-weight: 400;
    }
  }

  .value-card__number {
    position: absolute;
    top: 0;
    left: 0;

    width: 84px;
    height: 95px;

    display: flex;
    justify-content: center;
    align-items: center;

    font-family: Open Sans, sans-serif;
    font-size: 56px;
    font-weight: 700;

    color: #fff;

    background-image: url("../assets/number-back.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
}
</style>