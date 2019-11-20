<template>
    <div class="component home-header">
        <div class="container">
            <div class="logo">
                <img class="logo-el" :src="require('../../../assets/logo.png')" alt="美团">
            </div>
            <div class="search-input">
                <input-group></input-group>
                <div class="suggest-wrapper">
                    <a class="suggest-item hand hover">北京欢乐谷</a>
                    <a class="suggest-item hand hover">八达岭长城</a>
                    <a class="suggest-item hand hover">尚隐·泉都市生活馆</a>
                    <a class="suggest-item hand hover">圆明园</a>
                    <a class="suggest-item hand hover">香山公园</a>
                    <a class="suggest-item hand hover">德云社</a>
                    <a class="suggest-item hand hover">北宫国家森林公园</a>
                    <a class="suggest-item hand hover">中国国家博物馆</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import InputGroup from 'src/components/input-group'

export default {
    name: 'HomeHeader',
    components: {
        InputGroup
    }
}
</script>

<style lang="scss">
.component.home-header {
    background-color: #ffffff;
    padding-bottom: 50px;
    position: relative;

    &::after {
        position: absolute;
        content: " ";
        right: 0;
        bottom: 0;
        left: 0;
        height: 10px;
        z-index: -1;
        box-shadow: 0 2px 27px 0 rgba(0, 0, 0, .2);
    }

    .container {
        .logo {
            float: left;
            width: 126px;
            padding-top: 28px;
            .logo-el {
                width: 100%;
            }
        }
        .search-input {
            width: 550px;
            margin: 0 auto;
            padding-top: 28px;
            .suggest-wrapper {
                font-size: 12px;
                color: #999999;
                margin-top: 8px;
                padding-left: 12px;

                height: 18px;
                overflow: hidden;
                .suggest-item {
                    display: inline-block;
                    margin-right: 10px;
                }
            }
        }
    }
}
</style>
