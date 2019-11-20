<template>
    <dl class="component hotel">
        <dt class="title">酒店旅游</dt>
        <dd v-for="item in hotels" :key="item.href || item" class="hotel-item">
            <a :href="item.href || 'javascript:void(0);'" class="hover hand">{{item.label || item}}</a>
        </dd>
    </dl>
</template>

<script>
export default {
    name: 'Hotel',
    data () {
        return {
            hotels: [{
                href: '//www.qq.com',
                label: '国际机票'
            }, '火车票', '榛果民宿',
            '经济型酒店', '主题酒店', '商务酒店',
            '公寓', '豪华酒店', '客栈',
            '青年旅社', '度假酒店', '别野',
            '农家院']
        }
    }
}
</script>

<style lang="scss">
.component.hotel {
    display: inline-block;
    .title {
        text-align: center;
        font-size: 14px;
        color: #222222;
        font-weight: 500;
        margin-bottom: 26px;
    }
    .hotel-item {
        display: inline-block;
        width: 77px;
        height: 27px;
        line-height: 27px;
        text-align: center;
    }
}
</style>
