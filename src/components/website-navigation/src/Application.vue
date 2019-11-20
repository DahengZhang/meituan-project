<template>
    <dl class="component application">
        <dt class="title">手机应用</dt>
        <dd v-for="item in apps" :key="item.label" class="app-item"><a :href="item.href || 'javascript:void(0);'" class="hand"><img class="app-icon-el" :src="item.img" :alt="item.label"></a></dd>
    </dl>
</template>

<script>
export default {
    name: 'Application',
    data () {
        return {
            apps: [{
                href: '//bj.meituan.com',
                label: '美团',
                img: require('../../../assets/meituan.png')
            }, {
                label: '外卖',
                img: require('../../../assets/waimai.png')
            }, {
                label: '榛果',
                img: require('../../../assets/zhenguo.png')
            }, {
                label: '点评',
                img: require('../../../assets/dianping.png')
            }, {
                label: '猫眼',
                img: require('../../../assets/maoyan.png')
            }]
        }
    }
}
</script>

<style lang="scss">
.component.application {
    .title {
        text-align: center;
        font-size: 14px;
        color: #222222;
        font-weight: 500;
        margin-bottom: 26px;
    }
    .app-item {
        display: inline-block;
        width: 60px;
        height: 60px;
        margin: 0 8px;
        .app-icon-el {
            width: 100%;
        }
    }
}
</style>
