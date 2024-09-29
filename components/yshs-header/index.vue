<template>
    <div class="header">
        <div class="top content">
            <div class="Welcome">
                <div>您好 , 欢迎来到淘手游</div>
                <div class="line"></div>
                <div class="phone">
                    <div class="logo">
                        <img src="../../assets/images/mobile.png">
                    </div>
                    <div class="text">手机端</div>
                </div>
                <div class="phone">
                    <div class="logo">
                        <img src="../../assets/images/safeguard.png">
                    </div>
                    <div class="text">安全保障</div>
                </div>

            </div>
            <div class="login ">
                <div><a>登录</a></div>
                <i class="line"></i>
                <div><a>注册</a></div>
                <i class="line"></i>
                <div><a>个人中心</a></div>
                <i class="line"></i>
                <div><a>我是买家</a></div>
                <i class="line"></i>
                <div><a>我是卖家</a></div>
                <i class="line"></i>
                <div><a>收藏夹</a></div>
                <i class="line"></i>
                <div><a>消息中心</a></div>
                <i class="line"></i>
                <div class="app">
                    <img src="../../assets/images/mobile.png">
                    <a>App下载</a>
                </div>
            </div>
        </div>
    </div>
    <div class="searchblock content">
        <div class="logo">
            <img src="../../assets/images/logo.png">
        </div>
        <div class="search-hot">
            <form action="/game/search" class="search" id="search-form">
                <div class="search-box">
                    <input autocomplete="off" id="game-search" name="wd" class="search-inp" placeholder="请输入游戏名称">
                    <button class="searchbutton" type="submit">
                        <img src="../../assets//images/search.png">
                        <span>搜索</span>
                    </button>
                </div>
            </form>
            <div class="hot">
                <span>热门搜索:</span>
                <a>王者荣耀</a>
                <a>原神</a>
                <a>和平精英</a>
                <a>崩坏：星穹铁道</a>
                <a>航海王：燃烧意志</a>
                <a>晶核</a>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
</script>

<style lang="less">
.header {
    color: #fff;
    background-color: #F44145;
    height: 40px;

    .top {
        display: flex;
        align-items: center;
        justify-content: space-between;

        .Welcome {
            display: flex;
            align-items: center;
            text-align: center;

            .line {
                height: 12px;
                width: 1px;
                margin: 0 15px;
                background-color: #F98A8C;
            }

            .phone {
                display: flex;
                align-items: center;
                text-align: center;
            }

            .phone:last-child {
                padding-left: 20px;
            }
        }

        .login {
            display: flex;
            align-items: center;

            .line {
                height: 12px;
                width: 1px;
                margin: 0 15px;
                background-color: #F98A8C;
            }

            .app {
                display: flex;
            }
        }
    }

}

.searchblock {
    background-color: #fff;
    padding: 30px 0;
    display: flex;
    justify-content: space-between;

    .logo {
        margin-left: 5px;
    }

    .search-hot {
        width: 660px;

        .search-box {
            border-radius: 5px;
            overflow: hidden;
            border: 2px solid #F44145;
            height: 40px;
            box-sizing: border-box;
            display: flex;
            align-items: center;

            .search-inp {
                width: 560px;
                border: none;
                outline: none;
                box-sizing: border-box;
                padding: 13px 15px;
                font-size: 14px;
            }

            .searchbutton {
                background-color: #F44145;
                border: none;
                outline: none;
                width: 100px;
                color: #fff;
                font-size: 16px;
                align-self: stretch;
                display: flex;
                align-items: center;
                justify-content: center;

                span {
                    padding-left: 5px;
                }
            }
        }

        .hot {
            margin-top: 8px;
            font-size: 12px;
            white-space: nowrap;
            overflow: hidden;
          
            span {
                color: #999;
                margin-right: 15px;
            }

            a {
                margin-right: 15px;
            }
        }
    }
}
</style>