<template>
<div id="app">
  <h2>刘尔富实验室</h2>
  <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
    <el-menu-item index="1">主页</el-menu-item>
    <el-menu-item index="2">新闻</el-menu-item>
    <el-menu-item index="3">成员</el-menu-item>
    <el-menu-item index="4">论文</el-menu-item>
    <el-menu-item index="5">研究领域</el-menu-item>
    <el-menu-item index="6">招生招聘</el-menu-item>
  </el-menu>
  <el-carousel indicator-position="outside">
    <el-carousel-item v-for="item in 4" :key="item">
      <h3><img src="assets/logo.png"></h3>
    </el-carousel-item>
  </el-carousel>
</div>
</template>

<script>

export default {
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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n+1) {
  background-color: #d3dce6;
}
</style>
