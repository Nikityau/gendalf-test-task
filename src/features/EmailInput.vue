<script setup>
import Input from "@/shared/ui/Input.vue";
import {onMounted} from "vue";

const isEmail = defineModel('isEmail')
const isEL0 = defineModel('isEL0')

onMounted(() => {
  isEmail.value = false
  isEL0.value = false
})

const onChange = (value) => {
  isEL0.value = value.length === 0;

  const regex = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|.(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
  if (regex.test(value)) {
    isEmail.value = true

    return
  }

  isEmail.value = false
}

</script>
<template>
  <div
      class="email-input"
      :class="{
        'input__false': !isEL0 && !isEmail,
        'input__true': !isEL0 && isEmail,
      }"
  >
    <Input
        placeholder="Email"
        @onChange="onChange"
    />
    <div v-if="!isEL0 && isEmail" class="phone-input__mark">
      <svg width="31" height="31" viewBox="0 0 31 31" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="15.5" cy="15.5" r="15.5" fill="#9BCC37"/>
        <path
            d="M12.9982 18.209C13.1386 18.0687 13.2141 17.9931 13.3113 17.8852C16.0105 15.1107 18.7096 12.347 21.4087 9.57251C21.7326 9.23784 22.0889 8.98954 22.5532 9.00034C23.1254 9.00034 23.5573 9.27023 23.8272 9.78842C24.0971 10.3066 24.0431 10.8248 23.7192 11.3106C23.622 11.451 23.5033 11.5697 23.3845 11.6885C20.3183 14.8408 17.2413 17.9823 14.175 21.1346C13.3653 21.9551 12.5987 21.9551 11.7998 21.1346C10.3746 19.6664 8.9387 18.1982 7.51355 16.73C6.98452 16.1794 6.85496 15.5317 7.16806 14.9379C7.63231 14.0311 8.75515 13.88 9.51092 14.6465C10.5798 15.726 11.627 16.8164 12.6959 17.9067C12.7715 18.0039 12.8039 18.0255 12.9982 18.209Z"
            fill="white"/>
      </svg>
    </div>
    <div v-if="!isEL0 && !isEmail" class="phone-input__mark">
      <svg width="31" height="31" viewBox="0 0 31 31" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="15.5" cy="15.5" r="15.5" fill="#FD7583"/>
        <path
            d="M23.3538 9.13003L9.13049 23.3533C8.77361 23.7102 8.15162 23.6675 7.74211 23.258C7.3326 22.8485 7.28988 22.2265 7.64676 21.8696L21.8701 7.6463C22.2269 7.28942 22.8489 7.33214 23.2584 7.74165C23.6679 8.15116 23.7107 8.77315 23.3538 9.13003Z"
            fill="white"/>
        <path
            d="M21.8712 23.3535L7.64789 9.13024C7.29101 8.77337 7.33373 8.15138 7.74324 7.74187C8.15275 7.33235 8.77474 7.28964 9.13162 7.64651L23.3549 21.8698C23.7118 22.2267 23.6691 22.8487 23.2596 23.2582C22.8501 23.6677 22.2281 23.7104 21.8712 23.3535Z"
            fill="white"/>
      </svg>
    </div>
  </div>
</template>
<style>
.email-input {
  position: relative;

  .phone-input__mark {
    position: absolute;
    top: 50%;
    right: 0;

    transform: translate(-60%, -50%);
  }
}
</style>