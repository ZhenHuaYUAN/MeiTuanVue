<template>
  <div></div>
</template>

<script>
export default {
  layout: "blank",
  // 中间件使自定义函数在渲染页面之前自动执行
  middleware: async ctx => {
    let { status, data } = await ctx.$axios.get(
      "http://127.0.0.1:3000/users/exit"
    );
    if (status === 200 && data && data.code === 0) {
      window.location.href = "/";
    }
  }
};
</script>

<style>
</style>
