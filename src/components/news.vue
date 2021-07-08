<template>
    <div class="rowNews">
        <div class="rowNews__img">
            <img :src="image" alt="">
        </div>
        <div class="rowNews__info">
            <i-title  :title="title" />
            <i-label  :label="label" />
            <i-date   :date="date" />
        </div>
    </div>
</template>


<script>
import iTitle from './iNewsTitle.vue'
import iLabel from './iLabel.vue'
import iDate from './iDate.vue'

export default {
    name : 'rowNews',
    props:{
        image:{
        type: String,
        default: ''
        },
        label : {
            label : String,
            default : ''
        },
        date : {
            label : Date,
            default : `${new Date().getDate()} days ago`
        },
        title:{
            type : String,
            default : ''
        },
    },
    components : {
        iTitle,
        iLabel,
        iDate,
    }
}
</script>

<style lang="scss">
.rowNews{
    padding: 16px;
    border-radius: 16px;
    display: flex;
    align-items: center;
    gap: 24px;
    transition: ease-out 0.4s;
    &:hover{
        background: #ddeeff;
    }
    &__img{
        width: 82px;
        height: 82px;
        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 10px;
        }
    }
    &__info{
        display: flex;
        flex-direction: column;
        gap: 6px;
    }
}
</style>