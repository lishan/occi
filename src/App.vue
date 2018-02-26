<template>
  <div id="app">
    <el-menu
      :default-active="activeIndex2"
      class="el-menu-demo"
      mode="horizontal"
      @select="handleSelect"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b">
      <el-menu-item disabled class="opa1">
        <img style="height: 40px; width: 40px; margin-left: 20px;" src="./assets/logo.png">
        大数据智能运维平台
      </el-menu-item>
      <el-menu-item style="margin-left: 60px;" index="1">仪表盘</el-menu-item>
      <el-menu-item index="2">集群分析</el-menu-item>
      <el-menu-item index="3">租户分析</el-menu-item>
      <el-menu-item index="4">日志分析</el-menu-item>
      <el-submenu index="2">
        <template slot="title">智能优化</template>
        <el-menu-item index="2-1">Yarn计算资源配置优化</el-menu-item>
        <el-menu-item index="2-2">集群扩容推荐</el-menu-item>
        <el-menu-item index="2-3">集群拓扑结构</el-menu-item>
      </el-submenu>
      <el-menu-item class="pull-right">
        <i class="fa fa-user"></i>&nbsp;admin
      </el-menu-item>
      <el-menu-item class="pull-right">
        <i class="fa fa-question-circle"></i>&nbsp;帮助
      </el-menu-item>
    </el-menu>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1'
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style>
  html,body{
    margin: 0;
  }
  .opa1{
    opacity: 1 !important;
    cursor: default !important;
  }
  .pull-right{
    float: right !important;
  }
</style>
