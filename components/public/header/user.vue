<template>
  <div class="m-user">
    <!-- 需要判断是否登录 -->
    <template v-if="user">
      欢迎您，
      <span class="userName">{{ user }}</span>
      [
      <nuxt-link to="/exit">退出</nuxt-link>]
    </template>
    <template v-else>
      <nuxt-link to="/login" class="login">立即登录</nuxt-link>
      <nuxt-link class="register" to="/register" style="color:#999">注册</nuxt-link>
    </template>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: ""
    };
  }
};
</script>

<style>
</style>
