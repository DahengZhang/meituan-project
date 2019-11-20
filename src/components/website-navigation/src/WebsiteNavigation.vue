<template>
    <div class="component website-navigation">
        <hotel class="navigation-item hotel"></hotel>
        <dish class="navigation-item dish"></dish>
        <movie class="navigation-item movie"></movie>
        <application class="navigation-item application"></application>
    </div>
</template>

<script>
import Hotel from './Hotel'
import Dish from './Dish'
import Movie from './Movie'
import Application from './Application'

export default {
    name: 'WebsiteNavigtion',
    components: {
        Hotel,
        Dish,
        Movie,
        Application
    }
}
</script>

<style lang="scss">
.component.website-navigation {
    padding: 35px;
    .navigation-item {
        display: inline-block;
        vertical-align: top;
        margin-right: 47px;
        &:nth-last-of-type(1) {
            margin-right: 0;
        }
        &.hotel {
            width: 234px;
        }
        &.dish {
            width: 156px;
        }
        &.movie {
            width: 90px;
        }
        &.application {
            margin-left: 65px;
        }
    }
}
</style>
