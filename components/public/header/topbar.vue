<template>
<!-- elementUI 的分栏布局 一共24个栅格  gutter 属性来指定每一栏之间的间隔，默认间隔为 0。-->
    <el-row :gutter="0" class="m-header" style="color:#999">
      <el-col :span="5" >
        <geo></geo>
      </el-col>
      <el-col :span="5">
        <user></user>
      </el-col>
      <el-col :span="14">
        <navbar></navbar>
      </el-col>
    </el-row>
</template>

<script>
import Geo from './geo.vue'
import User from './user.vue'
import Navbar from './nav.vue'
export default {
  components:{
    Geo,
    User,
    Navbar
  }
};
</script>

<style lang="scss">
  @import "@/assets/css/public/layout.scss";
  @import "@/assets/css/public/header/index.scss";
</style>
