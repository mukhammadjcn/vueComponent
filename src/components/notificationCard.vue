<template>
  <div class="component">
    <div class="component__header">
      <h2 class="title">Notification</h2>
      <button @click="refresh()" class="btn">View</button>
    </div>
    <div class="row">
      <news v-for="(item, index) in notifications.sort(() => Math.random() - 0.5)"
                   :key="index" 
                   :title="item.title"
                   :label="item.label"
                   :date="item.date"
                   :image="item.image"
                   :read-time="item.readTime"/>
    </div>
    <span class="top-border">
      <svg width="32" height="13" viewBox="0 0 32 13" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M10.3432 2.65685L0 13H32L21.6569 2.65686C18.5327 -0.467339 13.4673 -0.467344 10.3432 2.65685Z" fill="#FCFCFD"/>
      </svg>
    </span>
  </div>
</template>

<script>
import News from './news.vue'

export default {
  name: "HelloWorld",
  components : {
    News,
  },
  methods : {
    refresh(){
      window.location.reload()
    },
  },
  data(){
    return {
      notifications : [
        {
          id : 1,
          title : 'ETH received',
          label : "0.08 ETH recived",
          date  : `${new Date().getDate()} days ago`,
          image : 'https://picsum.photos/100/100'
        },
        {
          id : 2,
          title : 'ETH received',
          label : "0.76 ETH recived",
          date  : `${new Date().getDate() + 1} days ago`,
          image : 'https://picsum.photos/100/101'
        },
        {
          id : 3,
          title : 'ETH send',
          label : "1.23 ETH recived",
          date  : `${new Date().getDate() -2} days ago`,
          image : 'https://picsum.photos/100/102'
        },
        {
          id : 4,
          title : 'ETH received',
          label : "0.61 ETH recived",
          date  : `${new Date().getDate() -5} days ago`,
          image : 'https://picsum.photos/100/103'
        },
        {
          id : 5,
          title : 'ETH send',
          label : "0.48 ETH recived",
          date  : `${new Date().getDate() + 10} days ago`,
          image : 'https://picsum.photos/100/104'
        },
        {
          id : 6,
          title : 'ETH received',
          label : "0.03 ETH recived",
          date  : `${new Date().getDate()} days ago`,
          image : 'https://picsum.photos/100/105'
        },
        {
          id : 7,
          title : 'ETH send',
          label : "0.99 ETH recived",
          date  : `${new Date().getDate() +1 } days ago`,
          image : 'https://picsum.photos/100/106'
        },
        {
          id : 8,
          title : 'ETH send',
          label : "0.54 ETH send",
          date  : `${new Date().getDate() +10 } days ago`,
          image : 'https://picsum.photos/100/107'
        },
        {
          id : 9,
          title : 'ETH recived',
          label : "0.92 ETH recived",
          date  : `${new Date().getDate() + 3 } days ago`,
          image : 'https://picsum.photos/100/108'
        },
        {
          id : 10,
          title : 'ETH send',
          label : "1.62 ETH recived",
          date  : `${new Date().getDate() -8 } days ago`,
          image : 'https://picsum.photos/100/109'
        },
        {
          id : 11,
          title : 'ETH send',
          label : "0.1 ETH send",
          date  : `${new Date().getDate() + 13 } days ago`,
          image : 'https://picsum.photos/100/110'
        },
        {
          id : 12,
          title : 'ETH send',
          label : "0.71 ETH send",
          date  : `${new Date().getDate() + 3 } days ago`,
          image : 'https://picsum.photos/100/111'
        },
        {
          id : 13,
          title : 'ETH recived',
          label : "0.66 ETH recived",
          date  : `${new Date().getDate()} days ago`,
          image : 'https://picsum.photos/100/112'
        },
        {
          id : 14,
          title : 'ETH recived',
          label : "1.99 ETH recived",
          date  : `${new Date().getDate() + 6 } days ago`,
          image : 'https://picsum.photos/100/113'
        },
        
      ]
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&display=swap');

.component{
  margin: 20px 0;
  position: relative;
  width: 396px;
  height: 528px;
  background: #FCFCFD;
  box-shadow: 0px 16px 64px -48px rgba(31, 47, 70, 0.4);
  border-radius: 10px;
  padding: 40px 32px;
  overflow-y: scroll;
  &__header{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-bottom: 24px;
    .title{
      font-family: DM Sans, sans-serif;
      font-style: normal;
      font-weight: bold;
      font-size: 32px;
      line-height: 40px;
      letter-spacing: -0.01em;
      color: #23262F;
    }
    .btn{
      padding: 12px 16px;
      background: #3772FF;
      border-radius: 90px;
      font-size: 14px;
      line-height: 16px;
      text-align: center;
      color: #FCFCFD;
      border: none;
      cursor: pointer;
      transition: ease-out 0.4s;
      &:hover{
        background-color: #1f62ff;
      }
    }
  }
}
.top-border{
  position: absolute;
    left: 50%;
    transform: translateX(-50%);
    top: -16px;
}

*::-webkit-scrollbar {
    width: 0;
  }
</style>
