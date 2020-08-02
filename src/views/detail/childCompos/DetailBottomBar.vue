<template>
  <div class="bottom-bar">
    <div class="bar-item bottom-left">
      <div>
        <i class="icon service"></i>
        <span class="text">客服</span>
      </div>
      <div>
        <i class="icon shop"></i>
        <span class="text">店铺</span>
      </div>
      <div>
        <i class="icon collect"></i>
        <span class="text">收藏</span>
      </div>
    </div>
    <div class="bottom-right">
      <div class="cart" @click="addToCart">加入购物车</div>
      <div class="buy">购买</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "DetailBottomBar",
    methods: {
      addToCart() {
        this.$emit('addCart')
      }
    }
  }
</script>

<style scoped>
  .bottom-bar {
   position: fixed;
    right: 0;
    left: 0;
    bottom: 0;
   display: flex;
    justify-content: space-around;
    background: whitesmoke;
    height: 49px;
  }
  .bar-item {
    display: flex;
    flex: 1;
  }
  .bar-item>div {
    flex: 1;
  }
  .bottom-left .text {
    font-size: 13px;
  }
  .bottom-left .icon {
    display: block;
    width: 22px;
    height: 22px;
    margin: 5px auto 3px;
    background: url("~assets/img/detail/detail_bottom.png") 0 0/100%;
  }
  .bottom-left .service {
    background-position: 0 -53px;
  }
  .bottom-left .shop {
    background-position: 0 -98px;
  }
  .bottom-left .collect {
    background-position: 0 1px;
  }
  .bottom-right{
    display: flex;
    align-items: center;
  }

  .cart{height: 40px;
    width: 90px;
    background:darkorange;
    color: white;
    border-radius: 10px 0 0 10px;
    padding-top: 10px;
    text-align: center;
  }
  .buy{height:40px;
    width: 90px;
    background: orangered;
    color: white;
    border-radius: 0 10px 10px 0;
    padding-top: 10px;
    text-align: center;
  }
  .text{
    position: relative;
    left: 19px;
  }
</style>
