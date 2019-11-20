<template>
    <div class="component input-group">
        <input type="text" placeholder="搜索商家或地点" class="search-input-el"><button class="search-btn-el hand"><i class="icon icon-search"></i></button>
    </div>
</template>

<script>
export default {
    name: 'InputGroup',
    props: {
        value: {
            type: String,
            default: ''
        }
    }
}
</script>

<style lang="scss">
.component.input-group {
    .search-input-el {
        box-sizing: border-box;
        width: 470px;
        height: 40px;
        padding: 0 10px;

        border: 1px solid #E5E5E5;
        border-right: none;
        border-radius: 4px 0 0 4px;

        vertical-align: top;
    }

    .search-btn-el {
        width: 80px;
        height: 40px;
        border: 0;
        border-bottom-right-radius: 4px;
        border-top-right-radius: 4px;
        background-color: #FFC300;

        .icon-search {
            font-size: 18px;
            color: #222222;
        }

        &:hover {
            background-color: $hover-yellow;
            .icon-search {
                color: #555555;
            }
        }

        &:active {
            background-color: $yellow;
            .icon-search {
                color: #ffffff;
            }
        }
    }
}
</style>
