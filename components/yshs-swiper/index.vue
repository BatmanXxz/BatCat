<template>
    <div class="main1 content">
        <div class="top ">
            <div class="allgame">
                <span>全部游戏</span>
                <a href="#">21857款手游
                    <img src="../../assets/images/all-game.png">
                </a>
            </div>
            <div class="nav-container">
                <ul class="nav">
                    <a href="#" class="item active">
                        <li>首页</li>
                    </a>
                    <a class="item active">
                        <li>端游账号</li>
                    </a>
                    <a class="item active">
                        <li>手游账号</li>
                    </a>
                    <a class="item active">
                        <li>开局自抽</li>
                    </a>
                    <a class="item active">
                        <li>首充号</li>
                    </a>
                    <a class="item active">
                        <li>首充号续冲</li>
                    </a>
                    <a class="item active">
                        <li>帮助中心</li>
                    </a>
                </ul>
            </div>
        </div>
    </div>
    <div class="main2">
        <div class="content">
            <!-- 束的导航栏 -->
            <div class="game">
                <div class="item">
                    <a>
                        <div class="item-con" v-for="(item, index) in gameitem" :key="index">
                            <div class="game-icon">
                                <img src="../../assets/images/wzry.jpg">
                            </div>
                            <div class="game-name">
                                <div class="line-1">王者荣耀</div>
                                <div class="tips">精品账号·永久包赔</div>
                            </div>
                            <img src="../../assets/images/more-game.png">
                        </div>
                    </a>
                </div>
            </div>
            <!-- 轮播图 -->
            <div class="swiper">
                <Swiper></Swiper>
            </div>
            <!-- 右边的登录消息 -->
            <div class="messageBox">

                <div class="infoBox">
                    <div class="userinfo">
                        <div class="adv">
                            <img style="width: 90px;height: 90px;margin: 0 auto;;" src="../../assets/images/5.jpg">
                        </div>
                        <div class="name">1006101510</div>
                    </div>

                    <div class="button">
                        <a href="#" class="buy"><span>我要买</span></a>
                        <a href="#" class="buy sell"><span>我要卖</span></a>
                    </div>

                    <!-- 公告栏 -->
                    <div class="notice">
                        <div class="title">官方公告</div>
                        <ul class="list">
                            <li v-for="(item, index) in notices" :key="index">
                                {{ item.text }}
                            </li>
                        </ul>
                    </div>

                    <!-- 下载广告 -->
                    <div class="downloadBox">

                        <div class="download">
                            <img src="../../assets/images/download.png">
                        </div>

                        <div class="text">
                            <div>下载淘手游APP</div>
                            <div class="downloadtext">游戏账号交易就上淘手游</div>
                        </div>

                    </div>



                    <div>


                    </div>
                </div>
            </div>


        </div>
    </div>
</template>

<script setup lang="ts">
const gameitem = ref([
    { name: "王者荣耀", imgage: '../../assets/images/more-game.png' },
    { name: "王者荣耀", imgage: '../../assets/images/more-game.png' },
    { name: "王者荣耀", imgage: '../../assets/images/more-game.png' },
    { name: "王者荣耀", imgage: '../../assets/images/more-game.png' },
    { name: "王者荣耀", imgage: '../../assets/images/more-game.png' },
    { name: "王者荣耀", imgage: '../../assets/images/more-game.png' }
])

const notices = ref([
    { text: "1、673联合法大大保障游戏账号交易安全", url: '' },
    { text: "2、重磅通知 淘手游升级终身包赔服务", url: '' },
    { text: "3、买号不被找回，才是淘手游的使命", url: '' },
    { text: "4、关于禁止未成年人参与交易申明", url: '' }
])

</script>

<style lang="less">
.main1 {
    .top {
        background-color: #fff;
        display: flex;

        .allgame {
            border-radius: 5px 5px 0px 0px;
            background-color: #F44145;
            width: 230px;
            height: 40px;
            padding: 12px 10px 12px 15px;
            box-sizing: border-box;
            color: #fff;
            display: flex;
            justify-content: space-between;

            span {
                font-size: 16px;
            }

            a {
                text-decoration: none;
                color: #fff;

                img {
                    align-self: center;
                    text-align: center;
                }
            }
        }

        .nav-container {
            align-self: stretch;

            .nav {
                padding: 0px 25px 0;
                font-size: 16px;
                line-height: 16px;
                align-items: center;
                display: flex;
                list-style: none;

                .item {
                    padding: 0 25px;
                    text-decoration: none;
                    color: #333;

                    li {
                        position: relative;
                    }


                }

                .active li::after {
                    content: '';
                    display: block;
                    position: absolute;
                    width: 100%;
                    bottom: -9px;
                    height: 4px;
                    border-radius: 2px;
                    background-color: #F44145;
                }
            }
        }
    }
}

.main2 {
    /* min-height: 713.25px; */
    background: url('../../assets/images/main-bg.png');

    .content {
        display: flex;

        .game {
            width: 230px;
            box-sizing: border-box;
            background-color: #fff;
            border-radius: 0 0 5px 5px;
            height: 456px;

            .item {
                height: 76px;
                cursor: pointer;
                box-sizing: border-box;
                border-bottom: 1px solid #F3F3F3;

                a {
                    text-decoration: none;
                    color: #333;

                    .item-con {
                        padding: 15px 10px 15px 15px;
                        display: flex;
                        align-items: center;
                        justify-content: space-between;

                        .game-icon {
                            width: 46px;
                            height: 46px;
                            border-radius: 15px;
                            overflow: hidden;

                            img {
                                width: 46px;
                            }
                        }

                        .game-name {
                            margin-left: -5px;
                            font-size: 14px;

                            .line-1 {
                                display: -webkit-box;
                                -webkit-box-orient: vertical;
                                text-overflow: ellipsis;
                                /* -webkit-line-clamp: 1; */
                                overflow: hidden;
                            }

                            .tips {
                                font-size: 12px;
                                color: #999;
                            }
                        }
                    }
                }
            }
        }

        .messageBox {
            width: 270px;
            margin-top: 10px;
            padding: 20px;
            background-color: #fff;
            border-radius: 5px;
            height: 446px;
            box-sizing: border-box;
        }

        .infoBox {
            align-items: center;
            text-align: center;

            .userinfo {
                .name {
                    font-size: 14px;
                    line-height: 14px;
                    text-align: center;
                    color: #F44145;
                }
            }

            .button {
                margin-top: 20px;
                display: flex;
                justify-content: space-between;

                .buy {
                    display: inline-block;
                    height: 36px;
                    font-size: 14px;
                    background-color: #F44145;
                    color: #fff;
                    border-radius: 5px;
                    box-sizing: border-box;
                    text-align: center;
                    line-height: 36px;
                    width: 115px;
                }

                .sell {
                    margin-left: 5px;
                    border: 1px solid #D8D8D8;
                    background-color: #fff;
                    color: #333;
                }
            }

            .notice {
                margin-top: 30px;
                text-align: left;

                .title {

                    font-size: 14px;
                    line-height: 14px;
                    color: #3D3D3D;
                    margin-bottom: 5px;
                }

                .list {
                    padding: 0;

                    li {
                        padding: 5px 0;
                        color: #999;
                        line-height: 12px;
                    }
                }
            }

            .downloadBox {
                cursor: pointer;
                border-radius: 5px;
                height: 67px;
                background: linear-gradient(105deg, #F44145 0%, #FF964A 99%);
                box-sizing: border-box;
                padding: 10px;
                display: flex;

                .text {
                    margin-left: 9px;
                    font-size: 20px;
                    line-height: 20px;
                    font-weight: bold;
                    color: #fff;
                    text-align: center;

                    .downloadtext {
                        font-size: 12px;
                        line-height: 12px;
                        font-weight: normal;
                        margin-top: 10px;
                    }
                }
            }
        }
    }

}
</style>