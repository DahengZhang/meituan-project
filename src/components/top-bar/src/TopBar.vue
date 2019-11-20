<template>
    <div class="component topbar">
        <div class="container">
            <div class="top-left">
                <i class="icon icon-position bar-item"></i>
                <span class="bar-item selected-city">北京</span>
                <a class="bar-item hand select-city">切换城市</a>
                [
                <div class="bar-item suggest-wapper">
                    <a class="suggest-item hover hand">门头沟</a>
                    <a class="suggest-item hover hand">大肠回族自治县</a>
                    <a class="suggest-item hover hand">廊坊</a>
                </div>
                ]
                <a class="bar-item hand sign in">立即登录</a>
                <a class="bar-item hand sign up hover">注册</a>
            </div>
            <div class="top-right">
                <div class="nav-list">
                    <dropdown-list
                        :label="'我的美团'"
                        :list="[{ href: '//www.baidu.com', label: '我的订单' }, '我的收藏', '抵用券', '账户设置']"
                        class="bar-item nav-item">
                    </dropdown-list>
                    <div class="bar-item nav-item">
                        <a href="" class="nav-link hover hand">
                            手机APP
                        </a>
                    </div>
                    <dropdown-list
                        :label="'商家中心'"
                        :width="'140%'"
                        :list="[{ href: '//www.baidu.com', label: '登录商家中心' }, '美团智能收银', '我想合作', '手机免费开店', '餐饮代理商招募', '商家申请开票', '免费合作美团排队']"
                        class="bar-item nav-item">
                    </dropdown-list>
                    <dropdown-list
                        :label="'美团规则'"
                        :list="['规则中心', '规则目录', '规则评议院']"
                        class="bar-item nav-item">
                    </dropdown-list>
                    <dropdown-list
                        :label="'网站导航'"
                        :width="'1200px'"
                        class="bar-item nav-item">
                        <website-navigation></website-navigation>
                    </dropdown-list>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import DropdownList from 'src/components/dropdown-list'
import WebsiteNavigation from 'src/components/website-navigation'

export default {
    name: 'TopBar',
    components: {
        DropdownList,
        WebsiteNavigation
    }
}
</script>


<style lang="scss">
.component.topbar {
    height: 40px;
    font-size: 12px;
    color: #999999;
    .container {
        .bar-item {
            display: inline-block;
        }
        .top-left {
            display: inline-block;
            padding-top: 12px;
            .icon {
                font-size: 12px;
            }
            .selected-city {
                color: #666666;
            }
            .select-city {
                background: #F4F4F4;
                border: 1px solid #E5E5E5;
                border-radius: 2px;
                color: #666666;
                display: inline-block;
                width: 57px;
                text-align: center;
                margin: 0 4px;
            }
            .suggest-wapper {
                .suggest-item {
                    display: inline-block;
                }
            }
            .sign {
                &.in {
                    color: $yellow;
                    margin-left: 25px;
                }
                &.up {
                    margin-left: 10px;
                }
            }
        }
        .top-right {
            float: right;
            .nav-list {
                font-size: 0;
                .nav-item {
                    box-sizing: border-box;
                    width: 78px;
                    height: 40px;
                    line-height: 40px;
                    text-align: center;
                    vertical-align: top;
                    .nav-link {
                        font-size: 12px;
                    }
                }
            }
        }
    }
}
</style>
