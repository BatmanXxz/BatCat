<template>
<div class="categoryBox content">
<div class="list" v-for="(item,index) in categorylist" :key="index">
    <img :src="item.src">
</div>
</div>
</template>

<script setup lang="ts">
import category1 from '../../assets/images/category1.png'
import category2 from '../../assets/images/category2.png'
import category3 from '../../assets/images/category3.png'
import category4 from '../../assets/images/category4.png'
const categorylist=ref([
    {
      src:category1,url:''
    },
    {
      src:category2,url:''
    },
    {
      src:category3,url:''
    },
    {
      src:category4,url:''
    }
])

</script>

<style lang="less">
.categoryBox{
    margin-top: 30px;
    display: flex;
    .list{
        margin: 10px auto 0;
    }
}
</style>