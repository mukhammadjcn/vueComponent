<template>
    <router-link :style="{'font-size': fontSize}"
                 :to = 'url'
                 class="iTitle">
        {{title}}
    </router-link>
</template>

<script>
export default{
    name : 'iTitle',
    props : {
        title:{
            type : String,
            default : 'title'
        },
        url:{
            type : String,
            default : '#'
        },
        fontSize:{
            type : String,
            default : '16px'
        },
        
    }
}
</script>


<style lang="scss">
.iTitle{
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
    color: #141416;
}
</style>