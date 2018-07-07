<template>
<div>
  <!-- 头部 -->
  <app-header></app-header>
  <div class="container-fluid">
    <div class="row">
     <!-- 侧边栏 -->
     <app-sidebar></app-sidebar>
      <div class="col-sm-9 col-sm-offset-3 col-md-10 col-md-offset-2 main">
        <h2 class="sub-header">Hero List</h2>
        <a class="btn btn-success" href="add.html">Add</a>
        <div class="table-responsive">
         <!-- 英雄列表 -->
          <app-heroes></app-heroes>
          <router-view></router-view>
        </div>
      </div>
    </div>
  </div>
</div>

</template>

<script>
// 导入单文件组件
import AppHeader from './components/AppHeader.vue'
import AppSidebar from './components/AppSidebar.vue'
import AppHeroes from './views/Heroes.vue'
// 导出
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  // 使用组件
  components:{
    AppHeader,
    AppSidebar,
    AppHeroes
  }
}
</script>

<style>

</style>
