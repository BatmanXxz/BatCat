<template>
    <div class="accountBox content">
        <div class="titleBox">
            <div class="title">精品账号</div>
            <div class="text">
                <div>账号找回</div>
                <div>永久包赔</div>
            </div>
        </div>

        <div class="routerBox">

            <div :class="['routerlist', currentIndex == index ? 'active' : '']" @click="changeCurrentIndex(index)"
                v-for="(item, index) in routerlist" :key="index">
                <div>{{ item.name }}</div>
            </div>
            <div class="routerlist">
                <a>全部游戏</a>
            </div>
        </div>
    </div>
    <Accountinfo :accountlist="accountlist"></Accountinfo>
</template>

<script setup lang="ts">
import tiod1 from '../../assets/images/tiod1.jpg'
const routerlist = ref(
    [
        {
            name: '王者荣耀', url: ''
        },
        {
            name: '原神', url: ''
        },
        {
            name: '地下城与勇士', url: ''
        },
        {
            name: '和平精英', url: ''
        },
        {
            name: '崩坏：星穹铁道', url: ''
        }
    ]
)
const currentIndex = ref(0)

const changeCurrentIndex = (index: number) => {
    currentIndex.value = index
}


const accountlist=[
    {
        name:'王者荣耀【安卓QQ】v10账号不想玩了低价出售',
        img:tiod1,
        ared:'安卓QQ|全部区服',
        money:'4500',
        online:'当前在线',
        isrealname:true,
        isrealman:true,
        isIndemnity:true
    },
    {
        name:'王者荣耀【安卓QQ】v10账号不想玩了低价出售',
        img:tiod1,
        ared:'安卓QQ|全部区服',
        money:'4500',
        online:'当前在线',
        isrealname:false,
        isrealman:true,
        isIndemnity:false
    },
    {
        name:'王者荣耀【安卓QQ】v10账号不想玩了低价出售',
        img:tiod1,
        ared:'安卓QQ|全部区服',
        money:'4500',
        online:'当前在线',
        isrealname:true,
        isrealman:false,
        isIndemnity:true
    },
    {
        name:'王者荣耀【安卓QQ】v10账号不想玩了低价出售',
        img:tiod1,
        ared:'安卓QQ|全部区服',
        money:'4500',
        online:'当前在线',
        isrealname:true,
        isrealman:true,
        isIndemnity:true
    },
    {
        name:'王者荣耀【安卓QQ】v10账号不想玩了低价出售',
        img:tiod1,
        ared:'安卓QQ|全部区服',
        money:'4500',
        online:'当前在线',
        isrealname:true,
        isrealman:true,
        isIndemnity:true
    },
    {
        name:'王者荣耀【安卓QQ】v10账号不想玩了低价出售',
        img:tiod1,
        ared:'安卓QQ|全部区服',
        money:'4500',
        online:'当前在线',
        isrealname:true,
        isrealman:true,
        isIndemnity:true
    },
    {
        name:'王者荣耀【安卓QQ】v10账号不想玩了低价出售',
        img:tiod1,
        ared:'安卓QQ|全部区服',
        money:'4500',
        online:'当前在线',
        isrealname:true,
        isrealman:true,
        isIndemnity:true
    },  
    {
        name:'王者荣耀【安卓QQ】v10账号不想玩了低价出售',
        img:tiod1,
        ared:'安卓QQ|全部区服',
        money:'4500',
        online:'当前在线',
        isrealname:true,
        isrealman:true,
        isIndemnity:true
    }          
]
</script>

<style lang="less">
.accountBox {
    margin-top: 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .titleBox {
        display: flex;

        .title {
            font-size: 28px;
            line-height: 28px;
            font-weight: bold;
            margin-right: 12px;
        }

        .text {
            color: #999;
            line-height: 16px;
        }
    }

    .routerBox {
        display: flex;
        margin-right: 33px;

        .routerlist {
            box-sizing: border-box;
            max-width: 124px;
            padding: 10px 14px;
            text-align: center;
            /* background-color: #FFF; */
            border-radius: 3px;
            margin-left: 10px;
            cursor: pointer;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
    }

    .active {
        background-color: #F44145;
        color: #fff;
    }
}
</style>