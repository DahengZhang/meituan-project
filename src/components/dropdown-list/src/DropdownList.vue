<template>
    <div class="component dropdown-list">
        <a :href="link || 'javascript:void(0);'" class="nav-link" :class="{'hand': link}">{{label}}</a>
        <ul class="dropdown-wrapper" :style="{ 'width': width }">
            <slot>
                <li v-for="item in list" :key="item.href || item" class="dropdown-item">
                    <a :href="item.href || 'javascript:void(0);'" class="dropdown-link hand">{{typeof item === 'string' ? item : item.label}}</a>
                </li>
            </slot>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'DropdownList',
    props: {
        link: {
            type: String,
            default: ''
        },
        label: {
            type: String,
            required: true
        },
        list: {
            type: Array,
            default: () => []
        },
        width: {
            type: String | Number,
            default: '100%'
        }
    }
}
</script>

<style lang="scss">
.component.dropdown-list {
    font-size: 12px;
    box-sizing: border-box;
    width: 78px;
    height: 40px;
    line-height: 40px;
    vertical-align: top;
    position: relative;
    z-index: 1;

    .nav-link {
        cursor: default;
    }

    .dropdown-wrapper {
        display: none;
        position: absolute;
        width: 100%;
        top: 95%;
        right: 0;
        background-color: #ffffff;
        box-shadow: 0 3px 5px 0 rgba(0,0,0,0.1);
        text-align: left;
        line-height: 1;
        .dropdown-item {
            text-align: center;
            line-height: 40px;
        }
        .dropdown-link {
            &:hover {
                color: $yellow;
            }
        }
    }

    &:hover {
        background-color: #fff;
        box-shadow: 0 3px 5px 0 rgba(0, 0, 0, .1);

        .nav-link {
            color: #FE8C00;
        }

        .dropdown-wrapper {
            display: block;
        }
    }
}
</style>
