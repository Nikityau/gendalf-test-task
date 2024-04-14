<script setup>
import Button from "@/shared/ui/Button.vue";

const {
  description,
  image
} = defineProps([
  'image',
  'description'
])
</script>
<template>
  <section class="live-card">
    <div
        class="live-card__preview"
        :style="{ 'backgroundImage': `url(${image})` }"
    >
    </div>
    <div class="live-card__info">
      <p>{{ description }}</p>
      <Button
        text="Перейти к статье"
        classnames="live-card__button"
      />
    </div>
  </section>
</template>
<style>
.live-card {
  width: 272px;

  border: 2px solid;
  border-radius: 5px;

  border-image-source: linear-gradient(161.98deg, #FFFFFF -3.6%, rgba(255, 255, 255, 0.2) 108.71%);

  background: linear-gradient(83.67deg, rgba(255, 255, 255, 0.16) 55.33%, rgba(7, 168, 219, 0.16) 98.64%);

  .live-card__preview {
    width: 100%;
    height: 191px;

    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;

    border-radius: 5px;
  }

  .live-card__info {
    text-align: left;

    padding: 25px;

    p {
      font-family: Open Sans, sans-serif;
      font-size: 18px;
      font-weight: 400;

      color: var(--color-gray);
    }

    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 10px;

    height: 170px;
  }

  .live-card__button {
    width: 100%;

    padding: 10px;

    text-align: center;

    font-size: 18px;
    font-weight: 400;

    color: var(--color-blue-l);
    border: 1px solid var(--color-blue-l);
  }
}
</style>
