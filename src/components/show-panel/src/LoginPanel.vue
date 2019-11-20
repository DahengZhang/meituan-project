<template>
    <div class="component login-panel">
        <button @click="next()">切换</button>
        <div class="wrapper">
            <transition>
                <template v-for="(item, index) in list">
                    <div v-if="show === index" :key="item.id" class="content">{{item.name}}</div>
                </template>
            </transition>
        </div>
    </div>
</template>

<script>
export default {
    name: 'LoginPanel',
    data () {
        return {
            show: 0,
            list: [{
                id: 0,
                name: 'This is One'
            }, {
                id: 1,
                name: 'This is Two'
            }, {
                id: 2,
                name: 'This is Three'
            }]
        }
    },
    methods: {
        next () {
            if (++this.show >= this.list.length) {
                this.show = 0
            }
        }
    }
}
</script>

<style lang="scss">
.component.login-panel {
    .v-enter-active, .v-leave-active {
        transition: opacity 2s;
    }

    .v-enter, .v-leave-to {
        opacity: 0;
    }

    .wrapper {
        position: relative;
        .content {
            position: absolute;
            background-color: rgba(0, 0, 0, .2);
        }
    }
}
</style>
