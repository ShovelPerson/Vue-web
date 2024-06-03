<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'

</script>

<template>

 



  <RouterView v-slot="{Component}" >
    <Transition name="fade" mode="out-in">
      <Component :is="Component"/>
    </Transition>
  </RouterView>
  

  <div class="wrapper">

      <nav>
        <button  > Change locale</button>
        <RouterLink to="/">
          <button > {{ $t('message.hello') }}</button>
        </RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
</template>
<style>
.fade-enter-from,.fade-leave-to{
  opacity: 0;
}
.fade-enter-active,.fade-leave-active{
  transition: opacity 0.5s ease-out ;
}
</style>

