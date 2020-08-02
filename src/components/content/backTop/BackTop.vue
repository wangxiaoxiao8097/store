<template>
  <div class="back-top">
    <img src="~assets/img/common/backtop.png" alt="">
  </div>
</template>

<script>
  export default {
    name: "BackTop",
    components:{},
  }
</script>

<style scoped>
  .back-top {
    position: fixed;
    right: 8px;
    bottom: 80px;
  }

  .back-top img {
    width: 28px;
    height: 80px;
  }
</style>
