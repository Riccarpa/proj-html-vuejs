<template>
  <div id="app">
   <Header/>
   <main>
     <Slider/>
   </main>
  </div>
</template>

<script>

import Header from '@/components/Header.vue';
import Slider from '@/components/Slider.vue';
export default {
  name: 'App',
  components: {
    Header,
    Slider
  }
}
</script>

<style lang="scss">
  @import 'bootstrap';
  @import './scss/_style.scss';
 
</style>
