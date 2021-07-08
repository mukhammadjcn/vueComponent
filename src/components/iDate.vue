<template>
    <router-link :style="{'font-size': fontSize}"
                 class="idate">
        {{date}}
    </router-link>
</template>

<script>
export default {
    name : 'iDate',
    props : {
        date : {
            label : Date,
            default : `${new Date().getDate()} days ago`
        }
    }
}
</script>

<style lang="scss">
.idate{
    font-size: 12px;
    line-height: 20px;
    color: #777E91;
}
</style>