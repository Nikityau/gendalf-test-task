<script setup>
import cn from 'classnames'

const {classnames, text} = defineProps(['classnames', 'text'])
</script>

<template>
  <button
      class="button-ui"
      :class="cn(classnames)"
  >
    {{ text }}
  </button>
</template>

<style>
.button-ui {
  border-radius: 5px;
  background: #fff;
  border: none;

  font-family: Open Sans, sans-serif;
  font-size: 18px;
  font-weight: 700;
}
</style>