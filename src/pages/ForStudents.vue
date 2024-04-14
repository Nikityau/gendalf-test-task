<script setup>

import Button from "@/shared/ui/Button.vue";
</script>

<template>
<article class="for-students">
  <div class="for-students__container">
      <h3>Ты студент и хочешь устроиться  на практику?</h3>
    <Button
      text="Оставить заявку"
      classnames="for-students__button_practice"
    />
  </div>
</article>
</template>

<style>
.for-students {
  width: 100%;
  height: 415px;

  @media screen and (max-width: 970px){
    height: auto;
  }

  background-image: url("../assets/students.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;

  .for-students__container {
    width: 100%;
    height: 100%;

    background-image: url("../assets/blue-filter.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 43px;



    h3 {
      max-width: 830px;

      font-family: Open Sans, sans-serif;
      font-size: 36px;
      font-weight: 700;

      color: #fff;

      text-align: center;
    }

    .for-students__button_practice {
      padding: 12px 30px;

      transition: all .3s ease-in-out;

      font-size: 18px;
      font-weight: 700;

      color: #fff;
      
      background: var(--color-green-l);
    }
    .for-students__button_practice:hover {
      background: var(--color-green-d);
    }

    @media screen and (max-width: 970px){
      gap: 20px;

      width: auto;
      height: auto;

      padding: 34px 40px 29px;

      h3 {
        font-size: 28px;
        font-weight: 300;
      }

      .for-students__button_practice {
        width: 100%;
      }
    }
  }
}
</style>
