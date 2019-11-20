<template>
    <div class="page home">
        <top-bar class="top-bar-el"></top-bar>
        <home-header class="home-header-el"></home-header>
        <div class="container main">
            <filter-panel class="filter-panel-el"></filter-panel>
            <show-panel class="show-panel-el"></show-panel>
        </div>
    </div>
</template>

<script>
import TopBar from 'src/components/top-bar'
import HomeHeader from 'src/components/home-header'
import FilterPanel from 'src/components/filter-panel'
import ShowPanel from 'src/components/show-panel'

export default {
    name: 'Home',
    data () {
        return {}
    },
    methods: {},
    components: {
        TopBar,
        HomeHeader,
        FilterPanel,
        ShowPanel
    }
}
</script>

<style lang="scss">
.page.home {
    .top-bar-el {}
    .home-header-el {}
    .main {
        position: relative;
        top: -50px;
        .filter-panel-el {
            display: inline-block;
            width: 230px;
        }
        .show-panel-el {
            display: inline-block;
            width: 950px;
            vertical-align: top;
            margin-left: 10px;
        }
    }
}
</style>
