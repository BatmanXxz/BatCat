<template>
    <div class="swiper">
        <Swiper
         ref="mySwiperRef"
         :modules="[SwiperAutoplay,SwiperNavigation,SwiperPagination]"
         :slides-per-view="1"
         :loop="true"
         :autoplay="{delay: 8000,disableOnInteraction: true,}" 
        @swiper="onSwiper"
        :pagination="{ clickable: true }"
  >
    <SwiperSlide v-for="(item,index) in imagse" :key="index">
      <img :src="item.img">
      <img src="https://img2.taoshouyou.com/tsyimg/sitesetting/banner/2024-04-29/19/71baf58d9fe1439db9b52163b9d0cc5b.jpg">
    </SwiperSlide>
  </Swiper>
  <div class="btns">
    <a  class="prev button"  @click="toPrev"><span><</span></a>
    <a  class="next button"  @click="toNext"><span>></span></a>
  </div>

    </div>
</template>

<script setup lang="ts">
import { Swiper,SwiperSlide } from 'swiper/vue';
import 'swiper/css'
import swiper1 from '../../assets/images/swiper1.jpg'
import swiper2 from '../../assets/images/swiper2.jpg'
let mySwiper:any = null;

const imagse=ref([{
    img:swiper1
},{img:swiper2}])

function toPrev(){
    mySwiper.slidePrev();
  }

  function toNext(){
    mySwiper.slideNext();
  }

  const onSwiper = (swiper:any) => {
    mySwiper = swiper;
  };
</script>

<style>
.swiper{
    width: 680px; 
    border-radius:5px;
    overflow: hidden;
    margin: 1px 10px 0;
    position: relative;
    height: 446px;
    --swiper-pagination-color: white;
    .swiper-pagination-bullet{
      width: 20px;
      height: 20px;
    }
}
.btns{
    margin-top:20px;
    a:hover{
    background-color: #333;
    }
    .prev{
      position: absolute;
      top: 50%;
      left: 10px;
      z-index: 99999;
      span{
        margin-left: 7px;
      }
    }
    .next{
      position: absolute;
      top: 50%;
      right: 10px;
      z-index: 99999;
      span{
        margin-left: 9px;
      }
    }
    span{
    margin-bottom: 2px;
    font-size: 25px;
    color: rgba(255, 255, 255, 0.8);
      }
    .button{
      width: 35px;
    height: 35px;
    border-radius: 50%;
    transform: translateY(-50%);
    background-color: rgba(0, 0, 0, .15);
    cursor: pointer;
    user-select: none;
    }  
  }
</style>