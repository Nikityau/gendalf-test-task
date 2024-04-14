<script setup>

</script>

<template>
<article class="for-developing">
  <h4>Инфраструктура для твоего развития и роста</h4>
  <div class="for-developing__container">
    <p>
      Мы создаем платформу для профессионального развития каждого сотрудника. Главная цель – дать возможность учиться, работать и получать удовольствие от каждой успешной задачи.
      О возможностях личностного роста в ГЭНДАЛЬФ расскажет руководитель Департамента персонала и карьеры Татьяна Арсенович.
    </p>
    <div class="for-developing__video">
      <img src="../assets/woman-2.png" alt="video-image-supa-dupa">
      <img class="for-developing__button" src="../assets/button.png" alt="video-button-supa-dupa">
    </div>
  </div>
</article>
</template>

<style>
.for-developing {
  padding: 61px 120px 49px 48px;

  background: linear-gradient(163.35deg, rgba(40, 228, 115, 0.16) 11.27%, rgba(70, 205, 22, 0.14) 35.82%, rgba(39, 221, 209, 0.39) 57.4%, rgba(5, 176, 213, 0.32) 82.7%);



  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 43px;

  h4 {
    font-family: Open Sans, sans-serif;
    font-size: 36px;
    font-weight: 300;

    color: var(--color-blue-l);
  }

  @media screen and (max-width: 970px){
    padding: 35px var(--side-padding) 23px;

    gap: 10px;

    h4 {
      font-size: 28px;
      font-weight: 400;

      text-align: center;
    }
  }

  .for-developing__container {
    width: 100%;

    display: flex;
    align-items: flex-start;
    justify-content: space-between;

    p {
      max-width: 495px;

      font-family: Open Sans, sans-serif;
      font-size: 18px;
      font-weight: 400;

      color: var(--color-gray);
    }

    .for-developing__video {
      position: relative;

      .for-developing__button {
        position: absolute;
        top: 50%;
        left: 50%;

        transform: translate(-50%, -50%);

        cursor: pointer;
      }
    }

    @media screen and (max-width: 970px){
      flex-direction: column;
      align-items: center;
      gap: 20px;

      p {
        max-width: 100%;

        font-size: 16px;
      }

      img {
        width: 100%;
      }

      .for-developing__button {
        width: 50px;
      }
    }
  }

}
</style>