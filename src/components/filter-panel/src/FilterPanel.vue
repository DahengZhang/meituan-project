<template>
    <div class="component filter-panel">
        <div class="title">全部分类</div>
        <ul class="filter-list-container">
            <li v-for="item in filterList" :key="item.icon" class="list-item">
                <a href="" v-for="i in item.labels" :key="i" class="fliter-link hand">{{i}}</a>
                <i class="icon icon-more"></i>
                <div class="filter-more">
                    asdasd
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'FilterPanel',
    data () {
        return {
            filterList: [{
                icon: 1,
                labels: ['美食']
            }, {
                icon: 2,
                labels: ['外卖']
            }, {
                icon: 3,
                labels: ['酒店']
            }, {
                icon: 4,
                labels: ['榛果民宿']
            }, {
                icon: 5,
                labels: ['猫眼电影']
            }, {
                icon: 6,
                labels: ['机票', '火车票']
            }, {
                icon: 7,
                labels: ['休闲娱乐', 'KTV']
            }, {
                icon: 8,
                labels: ['生活服务']
            }, {
                icon: 9,
                labels: ['丽人', '美发', '医学美容']
            }, {
                icon: 10,
                labels: ['结婚', '婚纱摄影', '婚宴']
            }, {
                icon: 11,
                labels: ['亲子', '儿童乐园', '幼教']
            }, {
                icon: 12,
                labels: ['运动健身', '健身中心']
            }, {
                icon: 13,
                labels: ['家装', '建材', '家居']
            }, {
                icon: 14,
                labels: ['学习培训', '音乐培训']
            }, {
                icon: 15,
                labels: ['医疗健康', '宠物', '爱车']
            }, {
                icon: 16,
                labels: ['酒吧', '密室逃脱']
            }]
        }
    }
}
</script>

<style lang="scss">
.component.filter-panel {
    box-sizing: border-box;
    border: 1px solid #E5E5E5;
    background-color: #ffffff;
    .title {
        line-height: 50px;
        color: #222222;
        font-weight: 600;
        box-sizing: border-box;
        padding-left: 15px;
    }
    .filter-list-container {
        font-size: 12px;
        color: #999999;
        padding: 10px 0 8px;
        position: relative;
        .list-item {
            line-height: 26px;
            padding: 0 12px;

            .fliter-link {
                position: relative;
                margin-right: 16px;
                &::after {
                    position: absolute;
                    content: "/";
                    right: -8px;
                }

                &:nth-last-of-type(1) {
                    &::after {
                        display: none;
                    }
                }

                &:hover {
                    color: #222222;
                }
            }

            .icon-more {
                float: right;
                line-height: 26px;
                font-size: 12px;
            }

            .filter-more {
                display: none;
                position: absolute;
                left: 100%;
                top: 10px;
                width: 400px;
                height: 425px;
                margin-left: 1px;
                z-index: 1;
                background-color: #ffffff;
            }

            &:hover {
                background-color: rgba(255, 150, 0, .08);
                .filter-more {
                    display: block;
                }
            }
        }
    }
}
</style>
