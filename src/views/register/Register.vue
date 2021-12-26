<template>
  <div class="warpper">
    <img src="#" alt="" class="warpper__img" />
    <div class="warpper__input">
      <input
        type="text"
        class="warpper__input__content"
        placeholder="请输入手机号"
      />
    </div>

    <div class="warpper__input">
      <input
        class="warpper__input__content"
        placeholder="请输入密码"
        type="password"
      />
    </div>
    <div class="warpper__input">
      <input
        class="warpper__input__content"
        placeholder="请确认密码"
        type="password"
      />
    </div>

    <div class="warpper__register-button">立刻注册</div>
    <div class="warpper__regerst-link" @click="handleLoginClick">
      已有账号？立刻登录
    </div>
  </div>
</template>
<script>
import { useRouter } from "vue-router";
export default {
  name: "register",
  setup() {
    const router = useRouter();
    const handleLoginClick = () => {
      router.push({ name: "Login" });
    };
    return { handleLoginClick };
  },
};
</script>

<style lang="scss" scoped>
@import "@/style/viriable.scss";
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
    padding: 0 0.16rem;
    background: #f9f9f9;
    border: 1px solid rgba(0, 0, 0, 0.1);
    border-radius: 0.06rem;
    &__content {
      border: none;
      outline: none;
      line-height: 00.48rem;
      width: 100%;
      background: none;
      font-size: 0.16rem;

      color: $content-notice-fontcolor;
      &::placeholder {
        color: $content-notice-fontcolor;
      }
    }
  }
  &__register-button {
    background: #0091ff;
    line-height: 0.48rem;
    font-size: 0.16rem;
    text-align: center;
    box-shadow: 0 0.04rem 0.08rem 0 rgba(0, 145, 255, 0.32);
    border-radius: 0.04rem;

    color: #fff;
    margin: 0.32rem 0.4rem 0.16rem 0.4rem;
  }
  &__regerst-link {
    font-size: 0.16rem;
    text-align: center;
    color: $content-notice-fontcolor;
  }
}
</style>
