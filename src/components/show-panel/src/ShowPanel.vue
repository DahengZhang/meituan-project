<template>
    <div class="component show-panel">
        <ul class="nav-wrapper">
            <li class="nav-item">
                <a href="" class="nav-link hand waimai">美团外卖</a>
            </li>
            <li class="nav-item">
                <a href="" class="nav-link hand maoyan">猫眼电影</a>
            </li>
            <li class="nav-item">
                <a href="" class="nav-link hand jiudian">美团酒店</a>
            </li>
            <li class="nav-item">
                <a href="" class="nav-link hand gongyu">民宿/公寓</a>
            </li>
            <li class="nav-item">
                <a href="" class="nav-link hand ruzhu">商家入住</a>
            </li>
            <li class="nav-item">
                <a href="" class="nav-link hand gongyi">美团公益</a>
            </li>
        </ul>
        <div class="show-container">
            <picture-panel
                :pictures="[{
                    label: 'waimai',
                    picture: 'http://p0.meituan.net/codeman/a97baf515235f4c5a2b1323a741e577185048.jpg'
                }, {
                    label: 'jiudian',
                    picture: 'http://p0.meituan.net/codeman/daa73310c9e57454dc97f0146640fd9f69772.jpg'
                }, {
                    label: 'meishi',
                    picture: 'http://p1.meituan.net/codeman/826a5ed09dab49af658c34624d75491861404.jpg'
                }, {
                    label: 'dianying',
                    picture: 'http://p0.meituan.net/codeman/33ff80dc00f832d697f3e20fc030799560495.jpg'
                }, {
                    label: 'paidui',
                    picture: 'https://p1.meituan.net/travelcube/01d2ab1efac6e2b7adcfcdf57b8cb5481085686.png'
                }]"
                class="picture-panel-el">
            </picture-panel>
        </div>
    </div>
</template>

<script>
import PicturePanel from 'src/components/picture-panel'

export default {
    name: 'ShowPanel',
    components: {
        PicturePanel
    }
}
</script>

<style lang="scss">
.component.show-panel {
    .nav-wrapper {
        .nav-item {
            display: inline-block;
            margin: 0 20px;
            line-height: 50px;
            .nav-link {
                color: #222;
                font-weight: 700;
                font-size: 16px;
                &.waimai {
                    &:hover {
                        color: #fbc700;
                    }
                }
                &.maoyan {
                    &:hover {
                        color: #ed1e24;
                    }
                }
                &.jiudian {
                    &:hover {
                        color: #f04d4e;
                    }
                }
                &.gongyu {
                    &:hover {
                        color: #fdc411;
                    }
                }
                &.ruzhu {
                    &:hover {
                        color: #fe8c00;
                    }
                }
                &.gongyi {
                    &:hover {
                        color: #f04d4e;
                    }
                }
            }
        }
    }
    .show-container {
        padding-top: 10px;
        .picture-panel-el {
            width: 550px;
            height: 240px;
        }
    }
}
</style>
