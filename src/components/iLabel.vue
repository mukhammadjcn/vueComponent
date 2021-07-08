<template>
    <router-link :style="{'font-size': fontSize}"
                 :to = 'url'
                 class="iLabel">
        {{label}}
    </router-link>
</template>

<script>
export default {
    name : 'iLabel',
    props : {
        label : {
            label : String,
            default : 'label'
        },
        url:{
            type : String,
            default : '#'
        },
    }
}
</script>

<style lang="scss">
.iLabel{
    font-weight: 500;
    font-size: 14px;
    line-height: 24px;
    color: #353945;
}
</style>