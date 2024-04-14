<script setup>
import {ref} from "vue";

const {
  radios,
  title
} = defineProps(['title', 'radios'])

const picked = ref()
</script>
<template>
<div class="radios">
  <h4>{{ title }}</h4>
  <div
      class="radios__el"
      v-for="r in radios"
  >
    <input type="radio" :id="r" :value="r" v-model="picked"/>
    <label :for="r">{{ r }}</label>
  </div>
</div>
</template>
<style>
.radios {
  width: 100%;

  margin: 17px 0;

  h4 {
    margin-bottom: 10px;

    font-family: Open Sans, sans-serif;
    font-size: 18px;
    font-weight: 700;

    color: #fff;
  }
  .radios__el {
    margin-bottom: 7px;

    font-family: Open Sans, sans-serif;
    font-size: 18px;
    font-weight: 400;

    color: #fff;

    display: flex;
    align-items: center;
    gap: 7px;

    input {
      width: 15px;
      height: 15px;
    }
  }
}
</style>