<template>
  <div id="app">
   <Header/>
   <main>
     <Slider :images="tasteSliderImg" />
     <ImgSection/>
   </main>
  </div>
</template>

<script>

import Header from '@/components/Header.vue';
import Slider from '@/components/Slider.vue';
import ImgSection from '@/components/ImgSection.vue';
export default {
  name: 'App',
  components: {
    Header,
    Slider,
    ImgSection
  },
  data(){
    return{
      tasteSliderImg:[
        {
          url:require('@/img/h3-rev-img-2.png'),
          bgUrl:require('@/img/h3-rev-img-1.png'),
          id:0
        },
        {
          url:require('@/img/h3-rev-img-4.png'),
          bgUrl:require('@/img/h3-rev-img-3.png'),
          id:1
        },
        {
          url:require('@/img/h3-rev-img-6.png'),
          bgUrl:require('@/img/h3-rev-img-5.png'),
          id:2
        },
      ],
    }
  }
}
</script>

<style lang="scss">
  @import 'bootstrap';
  @import './scss/_style.scss';
 
</style>
