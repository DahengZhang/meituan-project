<template>
    <dl class="component movie">
        <dt class="title">看电影</dt>
        <dd v-for="item in movies" :key="item.href || item" class="hotel-item">
            <a :href="item.href || 'javascript:void(0);'" class="hover hand">{{item.label || item}}</a>
        </dd>
    </dl>
</template>

<script>
export default {
    name: 'Movie',
    data () {
        return {
            movies: [{
                href: '//www.google.com',
                label: '热门电影'
            }, '热门影院', '热映电影口碑榜',
            '最受期待电影', '国内票房榜', '北美票房榜', '电影排行榜']
        }
    }
}
</script>

<style lang="scss">
.component.movie {
    .title {
        text-align: center;
        font-size: 14px;
        color: #222222;
        font-weight: 500;
        margin-bottom: 26px;
    }
    .hotel-item {
        display: inline-block;
        width: 90px;
        height: 27px;
        line-height: 27px;
        text-align: center;
    }
}
</style>
