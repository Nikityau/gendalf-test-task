<script setup>
import Button from "@/shared/ui/Button.vue";
import Navigation from "@/features/Navigation.vue";
</script>

<template>
  <header class="header">
    <div class="header__container">
      <img src="../assets/logo-desktop.png" alt="logo"/>
      <Navigation/>
    </div>
    <Button
        text="Запись на собеседование"
        classnames="header__button"
    />
  </header>
</template>
<style>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;

  padding: 13px var(--side-padding) 9px;

  background: var(--color-blue-l);

  @media screen and (max-width: 970px){
    display: none;
  }

  .header__container {
    display: flex;
    align-items: center;
    gap: 30px;
  }

  .header__button {
    font-weight: 400;
    color: var(--color-blue-l);

    padding: 8px 14px;

    border: 1px solid var(--color-blue-l);

    transition: all .3s ease;
  }
  .header__button:hover {
    color: var(--color-blue-d);
    border-color: var(--color-blue-d);
  }
}
</style>
