<template>
    <div class="itsBox content">
        <div class="issueBox">
            <div class="issueBox-title">
                <img src="../../assets/images/issue.png">
                <div class="title">常见问题</div>
            </div>
            <div class="list">
                <a class="item" v-for="(item, index) in Itclist" :key="index">
                    <div :class="['index', index == 0 ? 'index1' : '', index == 1 || index == 2 ? 'index2' : '']">{{
                        index + 1 }}</div>
                    <div class="name">{{ item.name }}</div>
                </a>
            </div>
        </div>


        <!-- 推荐 -->
        <div class="recommendBox">
            <div class="recommend-titleBox">
                <div class="recommend-title">
                    <div @mousemove="recommendMouse1" :class="['button', recommendIndex == 0 ? 'active' : '']">最新发布
                    </div>
                    <div @mousemove="recommendMouse2" :class="['button', recommendIndex == 1 ? 'active' : '']">严选推荐
                    </div>
                </div>

                <div class="download">
                    <img src="../../assets/images/down.png">
                    <div>下载APP查看更多</div>
                </div>

            </div>

            <div class="list">
                <div class="item" v-for="(item, index) in recommendIndex == 0 ? newlist : recommendlist">
                    <a class="imagesBox">
                        <img :src="item.img">
                    </a>
                    <a class="detail">
                        <div class="title line-1">{{ item.name }}</div>
                        <div class="line-1">{{ item.ared }}</div>
                        <div class="moneyBox">
                            <div>￥<span class="money">{{ item.money }}</span></div>
                            <div class="online">{{ item.online }}</div>
                        </div>
                        <div>

                        </div>

                        <div class="tag">
                            <div class="tag-item tag-compensate" v-if="item.isIndemnity == true">
                                <img src="../../assets/images/compensate.png">
                                <div>终身包赔</div>
                            </div>

                            <div class="tag-item tag-noCompensate" v-if="item.isIndemnity == false">
                                <img src="../../assets/images/sel-compensate.png">
                                <div>可购终身包赔</div>
                            </div>
                            <div class="tag-item tag-person" v-if="item.isrealman == true">
                                <img src="../../assets/images/person.png">
                                <div>已实人</div>
                            </div>

                            <div class="tag-item tag-name" v-if="item.isrealname == true">
                                <img src="../../assets/images/name.png">
                                <div>已实名</div>
                            </div>
                        </div>
                    </a>
                </div>
            </div>
        </div>

        <!-- 安全 -->
         <div class="safeBox">
            <div class="safe-title">
                <div>安全引导</div>
            </div>

            <div></div>
         </div>
    </div>
</template>

<script setup lang="ts">
interface IItclist {
    name: string,
    url: string
}

interface list {
    ared: string,
    img: string
    name: string,
    money: string,
    online: string,
    isrealname: boolean
    isrealman: boolean
    isIndemnity: boolean
}


interface IProps {
    Itclist: IItclist[]
    newlist: list[]
    recommendlist: list[]
}
const props = withDefaults(defineProps<IProps>(), {
    Itclist: () => [],
    newlist: () => [],
    recommendlist: () => []
});

const recommendIndex = ref(0)
const recommendMouse1 = () => {
    recommendIndex.value = 0
}
const recommendMouse2 = () => {
    recommendIndex.value = 1
}

const s = ref()
const b = ref()
</script>

<style lang="less">
.itsBox {
    display: flex;
}

.issueBox {
    border-radius: 5px;
    background-color: #fff;
    width: 260px;
    background: #fff url(../../assets/images/issue-bg.png) no-repeat;

    .issueBox-title {
        display: flex;
        padding: 10px 10px 0;
        align-items: center;

        .title {
            font-size: 20px;
            font-weight: bold;
            margin-left: 5px;
        }
    }

    .list {
        margin-top: 10px;
        padding: 13px 12px;
        border-radius: 10px 10px 5px 5px;
        background-color: #fff;
        font-size: 14px;
        color: #666;

        .item {
            display: flex;
            padding: 6px 0;
            align-items: center;

            .index {
                color: #3D3D3D;
                margin-right: 10px;
                width: 28px;
                height: 28px;
                text-align: center;
                line-height: 28px;
                ;
            }

            .index1 {
                background: url(../../assets/images/issue-no.png) no-repeat;
                color: #fff;
            }

            .index2 {
                background: url(../../assets/images/issue-no2.png) no-repeat;
                color: #fff;
            }
        }
    }
}

.recommendBox {
    margin: 0 10px 0;
    box-sizing: border-box;
    background: #fff url(../../assets/images/new-strict.png) no-repeat;
    padding: 20px 20px 11px;
    width: 660px;
    overflow: hidden;
    border-radius: 5px;

    .recommend-titleBox {
        display: flex;
        justify-content: space-between;

        .recommend-title {
            display: flex;

            .button {
                cursor: pointer;
                color: #999;
                padding: 11px 15px 13px;
                font-size: 20px;
            }

            .active {
                font-weight: bold;
                color: #333;
                background-color: #fff;
                border-radius: 10px 10px 0 0;
            }
        }

        .download {
            display: flex;
            font-size: 14px;
            color: #FF7667;
            padding: 7px 9px;
            border-radius: 5px;
            background-color: #fff;
            position: relative;
            width: 154px;
            height: 32px;
            box-sizing: border-box;
            margin-top: 10px;

            div {
                margin-left: 7px;
            }
        }
    }

    .list {
        padding: 15px 15px 0;
        background-color: #fff;
        border-top-right-radius: 10px;

        .item {
            margin-bottom: 15px;
            /* align-items: center; */
            cursor: pointer;
            display: flex;

            .imagesBox {
                display: block;
                width: 210px;
                height: 105px;
                border-radius: 5px;
                overflow: hidden;

                img {
                    object-fit: cover;
                    vertical-align: top;
                    width: 100%;
                    height: 100%;
                }
            }

            .detail {
                margin-left: 15px;
                color: #999;
                align-self: stretch;
                flex-direction: column;
                justify-content: space-between;
                display: flex;

                .title {
                    color: #333;
                    font-size: 15px;
                    font-weight: bold;
                }

                .moneyBox {
                    color: #F44145;
                    font-size: 14px;
                    display: flex;
                    align-items: baseline;

                    /*  */
                    .money {
                        font-size: 20px
                    }

                    .online {
                        margin-left: 10px;
                        color: #999;
                        font-size: 12px
                    }
                }

                .tag {
                    display: flex;
                    margin-top: 10px;

                    .tag-item {
                        height: 24px;
                        box-sizing: border-box;
                        display: flex;
                        align-items: center;
                        justify-content: space-evenly;
                        border-radius: 5px;
                        margin-right: 5px;
                        border: 1px solid currentColor;
                        /* padding: 0 7px; */
                        font-size: 12px;
                        line-height: 12px;
                        box-sizing: border-box;
                        width: 75px;

                        img {
                            width: 20px;
                            height: 20px;
                        }
                    }

                    .tag-compensate {
                        color: #fff;
                        background: linear-gradient(270deg, #F44145 0%, #FF6C70 100%);
                        width: 81px;
                    }

                    .tag-person {
                        color: #74A6FA;
                        border-color: #74A6FA;

                        img {
                            width: 16px;
                            height: 16px;
                        }
                    }

                    .tag-name {
                        color: #41C28D;
                        border-color: #41C28D;

                        img {
                            width: 16px;
                            height: 16px;
                        }
                    }

                    .tag-noCompensate {
                        color: #F44145;
                        margin-right: 5px;
                        background: #fff;
                        border-color: #F44145;
                        width: 105px;

                        img {
                            width: 20px;
                            height: 20px;
                        }
                    }
                }
            }

        }

    }
}
</style>