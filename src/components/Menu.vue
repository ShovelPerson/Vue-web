<script setup>
import { useI18n } from 'vue-i18n'
const { locale } = useI18n()

import '../assets/menu.css';

const changeLocale = () => {
  locale.value = locale.value == 'en' ? 'pt' : 'en'
}
</script>


<template>
<div class="wrapper">
  <div class="main-menu-container-body">
    <div class="main-menu-container">
    <nav class="main-menu">
      <button @click="changeLocale"> {{ $t('message.changeLocale') }}</button>
      <RouterLink to="/">
        <button > {{ $t('message.hello') }}</button>
      </RouterLink>
      <RouterLink to="/about">
        <button class="main-menu-button"> stuff </button>
      </RouterLink>
    </nav>
  </div>
</div>
  </div>
  
</template>
