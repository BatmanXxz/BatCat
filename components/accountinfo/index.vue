<template>
    <div class="content">
        <div class="main ">
            <div class="infoBox  " v-for="(item, index) in accountlist" :key="index">
                <a class="img">
                    <img :src="item.img">
                </a>
                <div class="name">
                    <a>
                        {{ item.name }}
                    </a>
                </div>
                <div class="ared">
                    <a>
                        {{ item.ared }}
                    </a>
                </div>

                <div class="moneyBox">
                    <a>
                        ￥
                        <span class="money">
                            {{ item.money }}
                        </span>
                        <span class="online">
                            {{ item.online }}
                        </span>
                    </a>
                </div>

                <div class="tag">
                    <div class="tag-item tag-compensate" v-if="item.isIndemnity == true">
                        <img src="../../assets/images/compensate.png">
                        <div>终身包赔</div>
                    </div>

                    <div class="tag-item tag-person" v-if="item.isrealman == true">
                        <img src="../../assets/images/person.png">
                        <div>已实人</div>
                    </div>

                    <div class="tag-item tag-person" v-if="item.isrealman == true">
                        <img src="../../assets/images/name.png">
                        <div>已实名</div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<script setup lang="ts">


interface IAccountlist {
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
    accountlist: IAccountlist[]
}

const props = withDefaults(defineProps<IProps>(), {
    accountlist: () => [],
});
</script>

<style lang="less">
.main {
    margin-top: 20px;
    display: flex;
    flex-wrap: wrap;

    .infoBox {
        width: 280px;
        box-sizing: border-box;
        border-radius: 5px 5px 0 0;
        overflow: hidden;
        margin: 0 13.3px 20px 0;

        .img {
            display: block;
            width: 100%;
            height: 140px;
            overflow: hidden;
            border-radius: 5px 5px 0 0;
            width: 280px;

            img {
                object-fit: cover;
                width: 100%;
                height: 100%;
                width: 280px;
            }
        }

        .name {
            margin: 12px 0 10px;
            font-size: 14px;
            height: 38px
        }

        .ared {
            color: #999;
        }

        .moneyBox {
            margin-top: 10px;
            align-items: baseline;

            a {
                font-size: 14px;
                color: #F44145;
            }

            .money {
                font-size: 20px;
                line-height: 20px;
            }

            .online {
                color: #999;
                margin-left: 10px;
                font-size: 12px;
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
                img{
                    width: 16px;
                    height: 16px;
                }
            }

            .tag-name {
                color: #41C28D;
                border-color: #41C28D;
                img{
                    width: 16px;
                    height: 16px;
                }
            }
        }
    }
}
</style>