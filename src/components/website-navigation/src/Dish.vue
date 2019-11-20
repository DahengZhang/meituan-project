<template>
    <dl class="component dish">
        <dt class="title">吃美食</dt>
        <dd v-for="item in dishes" :key="item.href || item" class="hotel-item">
            <a :href="item.href || 'javascript:void(0);'" class="hover hand">{{item.label || item}}</a>
        </dd>
    </dl>
</template>

<script>
export default {
    name: 'Dish',
    data () {
        return {
            dishes: [{
                href: '//www.google.com',
                label: '烤鱼'
            }, '特色小吃', '烧烤',
            '自助餐', '火锅', '代金券']
        }
    }
}
</script>

<style lang="scss">
.component.dish {
    .title {
        text-align: center;
        font-size: 14px;
        color: #222222;
        font-weight: 500;
        margin-bottom: 26px;
    }
    .hotel-item {
        display: inline-block;
        width: 78px;
        height: 27px;
        line-height: 27px;
        text-align: center;
    }
}
</style>
