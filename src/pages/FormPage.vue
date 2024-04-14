<script setup>
import Input from "@/shared/ui/Input.vue";
import PhoneInput from "@/features/PhoneInput.vue";
import EmailInput from "@/features/EmailInput.vue";
import Button from "@/shared/ui/Button.vue";
import RadioButtons from "@/features/RadioButtons.vue";


const radios = [
  'Работа в офисе',
  'Стажировка',
  'Удаленная работа'
]

</script>
<template>
  <article class="form-page">
    <div class="form-page__container">
      <form class="form-page__form">
        <h3>Записаться на собеседование</h3>
        <div class="form-page__inputs">
          <Input
              placeholder="Как к вам обращаться?"
          />
          <PhoneInput/>
          <EmailInput/>
          <Input
              placeholder="Желаемая должность"
          />
        </div>
        <RadioButtons
            title="Выберите категорию занятости"
            :radios="radios"
        />
        <textarea
          placeholder="Ваши вопросы"
        >
        </textarea>
        <div class="form-page__buttons">
          <Button
              text="Прикрепить резюме"
              classnames="form-page__add-file"
          />
          <Button
              text="Записаться"
              classnames="form-page__singin"
          />
        </div>
      </form>
    </div>
  </article>
</template>
<style>
.form-page {
  background-image: url("../assets/computer.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;

  .form-page__container {
    display: flex;
    justify-content: center;
    align-items: center;

    padding: 61px var(--side-padding);

    background-image: url("../assets/blue-filter.png");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;

    .form-page__form {
      padding: 40px 130px 57px;



      background-image: url("../assets/blue.png");
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;

      display: flex;
      flex-direction: column;
      align-items: center;

      textarea {
        width: calc(100% - 20px);
        height: 108px;

        padding: 10px;

        resize: none;

        font-family: Open Sans, sans-serif;
        font-size: 18px;
        font-weight: 300;

        outline: none;

        color: var(--color-gray);

        border-radius: 5px;
        border: 2px solid var(--color-gray);
      }

      h3 {
        font-family: Open Sans, sans-serif;
        font-size: 36px;
        font-weight: 300;

        color: #fff;
      }

      .form-page__inputs {
        margin-top: 20px;

        display: flex;
        flex-direction: column;
        gap: 6px;
      }

      @media screen and (max-width: 970px){
        padding: 18px 20px 16px;
      }
    }

    .form-page__buttons {
      margin-top: 17px;

      width: 100%;

      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    @media screen and (max-width: 970px){
      h3 {
        text-align: center;

        font-size: 28px;
      }

      .form-page__inputs {
        width: 100%;
      }

      textarea {
        height: calc(50px - 20px);
      }

      .form-page__buttons {
        flex-direction: column;

        gap: 10px;
      }
    }
  }

  .form-page__add-file {
    font-size: 18px;
    font-weight: 700;

    background: #fff;

    padding: 12px 16px;

    display: flex;
    align-items: center;
    gap: 10px;

    transition: all .3s;

    color: var(--color-green-l);
    border: 2px solid var(--color-green-l);
  }

  .form-page__add-file:hover {
    color: var(--color-green-d);
    border-color: var(--color-green-d);
  }

  .form-page__add-file::after {
    content: url("../assets/Vector.png");
  }

  .form-page__singin {
    font-size: 18px;
    font-weight: 700;

    color: #fff;

    padding: 15px 30px;

    transition: all .3s;

    background: var(--color-green-l);
  }

  .form-page__singin:hover {
    background: var(--color-green-d);
  }

  @media screen and (max-width: 970px){
    .form-page__add-file,
    .form-page__singin {
      width: 100%;
    }
    .form-page__add-file {
      justify-content: center;
    }
  }
}
</style>