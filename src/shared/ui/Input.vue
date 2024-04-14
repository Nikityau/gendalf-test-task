<script setup>
import cn from "classnames";

const {
  value,
  classnames,
  placeholder,
} = defineProps(['placeholder', 'classnames'])


</script>
<template>
  <input
      class="input-ui"
      :class="cn(classnames)"
      :placeholder="placeholder"
      @input="$emit('onChange', $event.target.value)"
  />
</template>
<style>
.input-ui {
  width: calc(568px - 40px);
  height: 50px;

  outline: none;

  padding: 0 20px;

  @media screen and (max-width: 970px){
    width: calc(100% - 44px);
  }

  border-radius: 5px;
  border: 2px solid var(--color-gray);

  font-family: Open Sans, sans-serif;
  font-size: 18px;
  font-weight: 300;

  color: #000;
}

.input-ui::placeholder {
  color: var(--color-gray);
}
</style>