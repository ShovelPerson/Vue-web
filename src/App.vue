<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import NavMenu from './components/Menu.vue'
</script>

<template>





  <RouterView v-slot="{Component}" >
    <Transition name="fade" mode="out-in">
      <Component :is="Component"/>
    </Transition>
  </RouterView>

<NavMenu/>

</template>
<style>
.fade-enter-from,.fade-leave-to{
  opacity: 0;
}
.fade-enter-active,.fade-leave-active{
  transition: opacity 2s ease-out ;
}
</style>
