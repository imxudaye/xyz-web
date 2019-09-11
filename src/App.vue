<template>
  <el-container>
<!--    //头-->
    <el-header>
      <xyz-header></xyz-header>
    </el-header>

    <el-main>
      <xyz-body></xyz-body>
    </el-main>

    <el-footer>
      <xyz-footer></xyz-footer>
    </el-footer>

  </el-container>
</template>

<script>


import XyzHeader from "./components/xyz-header";
import XyzBody from "./components/xyz-body";
import XyzFooter from "./components/xyz-footer";
export default {
  name: 'app',
  components: {
    XyzFooter,
    XyzBody,
    XyzHeader

  }
}
</script>

<style>
.el-header,.el-footer{
  background-color: #B3C0D1;
  color: #333;
  text-align: center;
  line-height: 60px;
  border-radius: 4px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, .12), 0 0 6px rgba(0, 0, 0, .04);
}
  .el-main{
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
    border-radius: 4px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, .12), 0 0 6px rgba(0, 0, 0, .04);
  }
</style>
