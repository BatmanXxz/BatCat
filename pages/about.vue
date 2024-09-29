<template>
    <div>
        <h3>这是about</h3>
    </div>

    <div>
        <swiper-container>
  <swiper-slide>Slide 1</swiper-slide>
  <swiper-slide>Slide 2</swiper-slide>
  <swiper-slide>Slide 3</swiper-slide>
     </swiper-container>
    </div>

</template>

<script setup lang="ts">
import Swiper from 'swiper';
import { register } from 'swiper/element/bundle';
register()
/* 项目完成之后挂载 */
onMounted(()=>{
  let swiper=new Swiper('.swiper',{
    slidesPerView: 3,
  grid: {
    rows: 3,
  },
  mousewheel: {
    forceToAxis: true,
  },
  })
})
</script>
