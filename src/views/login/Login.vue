<template>
  <div class="warpper">
    <img src="#" alt="" class="warpper__img" />
    <div class="warpper__input">
      <input type="text" class="warpper__input__content" />
    </div>

    <div class="warpper__input">
      <input type="text" class="warpper__input__content" />
    </div>

    <div class="warpper__login-button">登录</div>
    <div class="warpper__regerst">立即注册</div>
  </div>
</template>
<script>
export default {
  name: "login",
};
</script>

<style lang="scss" scoped>
.warpper {
  position: absolute;
  top: 50%;
  left: 0;
  right: 0;
  transform: translateY(-50%);
  &__img {
    margin: 0 auto 0.4rem auto;
    width: 0.66rem;
    height: 0.66rem;
    display: block;
  }
  &__input {
    height: 0.48rem;
    margin: 0 0.4rem 0.16rem 0.4rem;
    background: #f9f9f9;
    border: 1px solid rgba(0, 0, 0, 0.1);
    border-radius: 0.06rem;
    &__content {
      line-height: 00.48rem;
      width: 100%;
    }
  }
}
</style>
