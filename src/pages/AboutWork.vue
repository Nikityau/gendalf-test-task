<script setup>

import Button from "@/shared/ui/Button.vue";
</script>


<template>
  <article class="about-work">
    <div class="about-work__container">
      <div class="about-work__info">
        <h3>О том, чем мы занимаемся</h3>
        <section>
          <p>
            ГЭНДАЛЬФ – один из крупнейших игроков на рынке информационных технологий, занимающий 4 место среди 7000
            партнеров фирмы «1С». У нас есть представительства в 15 городах России, а нашими услугами пользуются 23 000
            организаций-клиентов, в числе которых «Базэл Аэро», «Ростсельмаш», UTG. Аэропорт Кольцово и многие другие.

          </p>
          <p>
            Мы тщательно подходим к выбору сотрудников, которые становятся частью команды профессионалов.
          </p>
          <p>
            У нас работают специалисты разных областей: программисты, маркетологи, менеджеры, копирайтеры, методисты и
            другие, чей карьерный рост не ограничен привычными рамками.
          </p>
        </section>
        <div class="about-work__buttons">
          <Button
              text="Узнать больше"
              classnames="about-work__button_more"
          />
          <Button
              text="Записаться на собеседование"
              classnames="about-work__button_singin"
          />
        </div>
      </div>
      <img src="../assets/woman.png" alt="image">
    </div>
  </article>
</template>

<style>
.about-work {
  width: 100%;
  height: 100%;

  background: #fff;

  .about-work__container {
    padding: 50px var(--side-padding) 65px;

    display: flex;
    align-items: center;
    justify-content: space-between;

    .about-work__info {
      max-width: 720px;

      font-family: Open Sans, sans-serif;
      font-size: 36px;
      font-weight: 300;

      h3, p {
        margin-bottom: 20px;
      }

      h3 {
        font-weight: 300;
        color: var(--color-blue-l);
      }
      p {
        font-size: 18px;
        font-weight: 400;

        color: var(--color-gray);
      }
    }

    img {
      width: 550px;
    }

    @media screen and (max-width: 970px) {
      img {
        display: none;
      }

      justify-content: center;
      h3 {
        text-align: center;

        font-size: 28px;
        font-weight: 400;
      }
      p {
        font-size: 16px;
      }
    }
  }

  .about-work__buttons {
    display: flex;
    align-items: center;
    gap: 21px;

    @media screen and (max-width: 970px){
      flex-direction: column;
      gap: 10px;

      padding: 0 30px;
    }

    .about-work__button_more,
    .about-work__button_singin {
      padding: 13px 40px;

      font-size: 18px;
      font-weight: 700;

      color: #fff;

      transition: all .3s ease-in-out;

      background: var(--color-blue-l);

      @media screen and (max-width: 970px){
        width: 100%;
      }
    }
    .about-work__button_more:hover {
      background: var(--color-blue-d);
    }

    .about-work__button_singin {
      padding: 12px 17px;

      background: transparent;

      border: 1px solid var(--color-blue-l);
      color: var(--color-blue-l);
    }
    .about-work__button_singin:hover {
      border-color: var(--color-blue-d);
      color: var(--color-blue-d);
    }
  }
}
</style>