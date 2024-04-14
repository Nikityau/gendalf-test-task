<script setup>

import Button from "@/shared/ui/Button.vue";
</script>

<template>
  <article class="welcome">
    <div class="welcome__container">
      <h1>Добро пожаловать в ГЭНДАЛЬФ!</h1>
      <p>Мы готовы поделиться секретом, почему любим компанию, в которой работаем. Если тебе будут близки наши ценности
        и идеи, то смело записывайся на собеседование!</p>
      <div class="welcome__buttons">
        <Button
            text="Почему мы"
            classnames="welcome__button_we"
        />
        <Button
            text="Записаться на собеседование"
            classnames="welcome__button_singin"
        />
      </div>
    </div>
  </article>
</template>

<style>
.welcome {
  width: 100%;
  height: 568px;

  @media screen and (max-width: 970px){
    height: auto;
  }

  background-image: url("../assets/welcome.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;

  .welcome__container {
    width: 100%;
    height: 100%;

    @media screen and (max-width: 970px){
      width: auto;
      padding: 20px 35px;
    }

    background-image: url("../assets/blue-filter.png");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    h1, p, .welcome__buttons {
      max-width: 830px;

      font-family: Open Sans, sans-serif;
      font-size: 64px;
      font-weight: 700;

      color: #FFF;

      text-align: center;
    }

    h1 {
      margin-bottom: 20px;
    }

    p {
      font-size: 25px;
      font-weight: 400;

      margin-bottom: 43px;
    }

    .welcome__buttons {
      display: flex;
      align-items: center;
      gap: 63px;
    }

    @media screen and (max-width: 970px){
      h1 {
        font-size: 24px;
      }
      p {
        font-size: 16px;
        max-width: 355px;
      }

      .welcome__buttons {
        flex-direction: column;
        gap: 10px;
      }
    }
  }

  .welcome__button_we,
  .welcome__button_singin {
    padding: 12px 28px;

    font-size: 18px;
    font-weight: 700;

    color: #fff;

    background: var(--color-green-l);

    transition: all .3s ease-in-out;

    @media screen and (max-width: 970px){
      width: 100%;
    }
  }
  .welcome__button_we:hover {
    background: var(--color-green-d);
  }

  .welcome__button_singin {
    padding: 12px 13px;

    border: 1px solid var(--color-green-d);

    background: #fff;

    color: var(--color-green-l);
  }
  .welcome__button_singin:hover {
    color: var(--color-green-d);
    border-color: var(--color-green-d);
  }
}
</style>
