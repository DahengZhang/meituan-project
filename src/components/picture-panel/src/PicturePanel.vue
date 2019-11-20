<template>
    <div class="component picture-panel">
        <ul class="picture-list">
            <template v-for="(item, index) in pictures">
                <li v-if="index === nowShow" :key="item.label" class="picture-item">
                    <img :src="item.picture" class="picture-el" :alt="item.label">
                </li>
            </template>
        </ul>
        <i @click="previous()" class="icon hand icon-left"></i>
        <i @click="next()" class="icon hand icon-right"></i>
    </div>
</template>

<script>
export default {
    name: 'PicturePanel',
    props: {
        pictures: {
            type: Array,
            default: () => []
        }
    },
    data () {
        return {
            nowShow: 0
        }
    },
    methods: {
        previous () {
            if (--this.nowShow < 0) {
                this.nowShow = this.pictures.length - 1
            }
        },
        next () {
            if (++this.nowShow >= this.pictures.length) {
                this.nowShow = 0
            }
        }
    }
}
</script>

<style lang="scss">
.component.picture-panel {
    display: inline-block;
    box-sizing: border-box;
    background-color: rgba(0, 0, 0, .2);
    position: relative;
    &::after {
        content: "";
        display: inline-block;
        width: 0;
        height: 100%;
        vertical-align: middle;
    }
    .picture-list {
        display: inline-block;
        overflow: hidden;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        .picture-item {
            width: 100%;
            height: 100%;
            .picture-el {
                width: 100%;
                height: 100%;
            }
        }
    }
    .icon {
        display: none;
        vertical-align: middle;
        font-size: 45px;
        z-index: 9;
        position: relative;
        opacity: .5;
        border-radius: 50%;
        overflow: hidden;
        &.icon-right {
            left: 100%;
            margin-left: -94px;
        }
        &:hover {
            opacity: .8;
        }
    }
    &:hover {
        .icon {
            display: inline-block;
        }
    }
}
</style>
