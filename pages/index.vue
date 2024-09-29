<template>
  <YshsHeader></YshsHeader>
  <YshsSwiper></YshsSwiper>
  <Category></Category>
  <Account></Account>
  <Itc :Itclist="Itclist" :newlist="newlist" :recommendlist="recommendlist"></Itc>
</template>

<script setup lang="ts">
import tiod1 from '../assets/images/tiod1.jpg'
const Itclist = ref([
  {
    name: '买家购买后如何发货交易？', url: ''
  },
  {
    name: '下单后多久发货？', url: ''
  },
  {
    name: '如何更快的卖出商品', url: ''
  },
  {
    name: '商品卖出后多久能收到钱', url: ''
  },
  {
    name: '找回包赔有什么用？', url: ''
  },
  {
    name: '找回包赔怎么买？', url: ''
  },
  {
    name: '商品有问题怎么办？', url: ''
  },
  {
    name: '出售商品被申请仲裁怎么办？', url: ''
  },
  {
    name: '找回包赔申请流程', url: ''
  },
])

const newlist = ref([
  {
    name: '王者荣耀【安卓QQ】v10账号不想玩了低价出售',
    img: tiod1,
    ared: '安卓QQ|全部区服',
    money: '4500',
    online: '当前在线',
    isrealname: true,
    isrealman: true,
    isIndemnity: true
  },
  {
    name: '王者荣耀【安卓QQ】v10账号不想玩了低价出售',
    img: tiod1,
    ared: '安卓QQ|全部区服',
    money: '4500',
    online: '当前在线',
    isrealname: false,
    isrealman: true,
    isIndemnity: false
  },
  {
    name: '王者荣耀【安卓QQ】v10账号不想玩了低价出售',
    img: tiod1,
    ared: '安卓QQ|全部区服',
    money: '4500',
    online: '当前在线',
    isrealname: true,
    isrealman: true,
    isIndemnity: true
  },]
)
const recommendlist = ref([
  {
    name: '和平精英',
    img: tiod1,
    ared: '安卓QQ|全部区服',
    money: '4500',
    online: '当前在线',
    isrealname: true,
    isrealman: true,
    isIndemnity: true
  },
  {
    name: '和平精英',
    img: tiod1,
    ared: '安卓QQ|全部区服',
    money: '4500',
    online: '当前在线',
    isrealname: true,
    isrealman: true,
    isIndemnity: true
  },
  {
    name: '王者荣耀【安卓QQ】v10账号不想玩了低价出售',
    img: tiod1,
    ared: '安卓QQ|全部区服',
    money: '4500',
    online: '当前在线',
    isrealname: true,
    isrealman: true,
    isIndemnity: true
  },]
)
</script>

<style></style>