<script setup>
import {ref, watch} from "vue";

const {
  description,
  tips,
  title
} = defineProps(['title', 'description', 'tips'])

const isOpen = ref(false)
const refBott = ref(null)
const refBottContainer = ref(null)

watch(isOpen, () => {
  if (!isOpen.value) {
    refBott.value.style.height = 0

    return
  }

  refBott.value.style.height = `${refBottContainer.value.offsetHeight}px`
})

</script>

<template>
  <section class="hidden">
    <div class="hidden__header" @click="isOpen = !isOpen">
      <button
          class="hidden__btn"
          :class="{ 'hidden__btn_open':isOpen }"
      >
        <svg width="23" height="23" viewBox="0 0 23 23" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="11.5" cy="11.5" r="10.5" stroke="#00B7EC" stroke-width="2"/>
          <path
              d="M16.5 11.134C17.1667 11.5189 17.1667 12.4811 16.5 12.866L9 17.1962C8.33333 17.5811 7.5 17.0999 7.5 16.3301L7.5 7.66987C7.5 6.90007 8.33333 6.41895 9 6.80385L16.5 11.134Z"
              fill="#00B7EC"/>
        </svg>
      </button>
      <h4>{{ title }}</h4>
    </div>
    <div
        class="hidden__bottom"
        ref="refBott"
    >
      <div
          class="hidden__bottom-container"
          ref="refBottContainer"
      >
        <div class="plug"></div>
        <div class="hidden__text">
          <p>{{ description }}</p>
          <div class="hidden__tips-list">
            <section
                class="hidden__tip"
                v-for="tip in tips"
                :key="tip.id"
            >
              <p><span>{{ tip.title }}</span> {{ tip.tip }}</p>
            </section>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.hidden {
  .hidden__header {
    display: grid;
    grid-template-columns: 23px auto;
    align-items: center;
    gap: 15px;

    cursor: pointer;

    .hidden__btn {
      svg {
        width: 23px;
        height: 23px;

        transition: all .3s ease-in-out;
      }

      background: none;
      border: none;
    }

    .hidden__btn_open {
      svg {
        transform: rotate(90deg);
      }
    }

    h4 {
      font-family: Open Sans, sans-serif;
      font-size: 18px;
      font-weight: 400;

      color: var(--color-gray);

      text-decoration: underline;
    }

    margin-bottom: 8px;
  }

  .hidden__bottom {
    .hidden__bottom-container {
      display: grid;
      grid-template-columns: 23px auto;
      align-items: center;
      gap: 15px;
    }

    height: 0;
    overflow: hidden;

    transition: all .3s ease-in-out;

    font-family: Open Sans, sans-serif;
    font-size: 18px;
    font-weight: 400;

    color: var(--color-gray);

    .hidden__tips-list {
      padding-top: 10px;
      padding-left: 15px;
    }

    .hidden__tip {
      margin-bottom: 10px;

      span {
        position: relative;

        font-weight: 700;
      }

      span::before {
        content: '';

        position: absolute;
        top: 50%;
        left: 0;

        transform: translate(-13px, -50%);

        width: 6px;
        height: 6px;

        border-radius: 50%;

        background: var(--color-gray);
      }
    }
  }
}
</style>