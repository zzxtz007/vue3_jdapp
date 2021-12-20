<template>
  <div class="warpper">
    <div class="warpper__position">
      <span class="iconfont warpper__position__icon">&#xe7f1;</span>
      北京理工大学
      <span class="iconfont warpper__position__notice">&#xe60d;</span>
    </div>
    <input type="text" class="warpper__search" />
  </div>
  <div class="docker">
    <span class="docker__item docker__item--active">
      <div class="iconfont">&#xe7c6;</div>
      <div class="docker__title">首页</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe638;</div>
      <div class="docker__title">购物车</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe7b3;</div>
      <div class="docker__title">订单</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe635;</div>
      <div class="docker__title">我的</div>
    </span>
  </div>
</template>
<script>
export default {
  name: "home",
};
</script>

<style lang="scss" scoped>
@import "@/style/viriable.scss";
@import "@/style/mixins.scss";
.warpper {
  position: absolute;
  left: 0;
  top: 0%;
  bottom: 0.5rem;
  right: 0;
  padding: 0 0.18rem;
  color: $content-fontcolor;
  &__position {
    position: relative;
    @include esplice;
    padding: 0.16rem 0.24rem 0.16rem 0;
    line-height: 0.22rem;
    font-size: 0.16rem;
    &__icon {
      font-size: 0.2rem;
      position: relative;
      top: 0.01rem;
    }
    &__notice {
      position: absolute;
      font-size: 0.2rem;
      top: 0.17rem;
      right: 0;
    }
  }
  &__search {
    line-height: 0.32rem;
    background: #f5f5f5;
    color: #b7b7b7;
    border-radius: 0.16rem;
    border: #f5f5f5 1px solid;
    outline: none;
    font-size: 0.14rem;
    width: 100%;
    padding: 0 0.15rem 0 0.15rem;
  }
}

.docker {
  display: flex;
  box-sizing: border-box;
  position: absolute;
  left: 0;
  width: 100%;
  padding: 0 0.18rem;
  bottom: 0;
  height: 0.49rem;
  border-top: 1px solid #f1f1f1;
  color: $content-fontcolor;
  &__item {
    flex: 1;
    text-align: center;
    .iconfont {
      margin: 0.07rem 0 0.02rem 0;
      font-size: 0.18rem;
    }
    &--active {
      color: #1fa4fc;
    }
  }
  .docker__titel {
    font-size: 0.2rem;
    transform: scale(0.5 0.5);
    transform-origin: center top;
  }
}
</style>
