<template>
  <div id="app">
    <notification-card />
  </div>
</template>

<script>
import notificationCard from "./components/notificationCard.vue";

export default {
  name: "App",
  components: {
    notificationCard,
  },
};
</script>

<style lang="scss">
  body{
    background: #141416;
    font-family: 'DM Sans', sans-serif;
  }
  #app{
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
