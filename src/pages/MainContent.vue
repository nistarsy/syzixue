<template>
  <div class="mainContent">
    <el-breadcrumb separator="/" class="breadcrumb">
      <!-- <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
      <el-breadcrumb-item>活动列表</el-breadcrumb-item>
      <el-breadcrumb-item>活动详情</el-breadcrumb-item> -->
    <el-breadcrumb-item v-for="route in $route.matched"
    :key="route.path"
    >
    {{ route.meta.name }}
    </el-breadcrumb-item> 
    </el-breadcrumb>
    <router-view />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.breadcrumb {
  margin-top: 20px;
}
.mainContent {
  margin-left: 20px;
}
</style>