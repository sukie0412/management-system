<style>
.breadcrumb{
  height: 30px;
}
</style>

<template>
<!--   <div>
    <span class='title'>{{title}}</span>
    <ul class='breadcrumb'>
      <li v-for='{item,index} in breadList' :key='index'>
        <route-link :to='item.path'>{{item.meat.breadcrumbName}}f</route-link>
        <span class='separtor' v-if='index !== breadList.length-1'>ds{{separtor}}</span>
      </li>
    </ul>
  </div> -->
<!--     <div class="breadcrumb">
    <slot></slot>
  </div> -->
  <div class='breadcrumbNav'>
    <el-breadcrumb separator-class='el-icon-arrow-right' class='breadcrumb'>
      <el-breadcrumb-item :to="{path:'/'}"><i class='el-icon-location'></i>首页</el-breadcrumb-item>
      <el-breadcrumb-item>用户管理</el-breadcrumb-item>
      <el-breadcrumb-item>部门列表</el-breadcrumb-item>
    </el-breadcrumb>
    <hr/>
  </div>
</template>

<script>
export default{
  props: {
    separator: {
      type: String,
      default: '/'
    }
  }
  // 在实例创建完成后被立即调用
//   created () {
//     this.getBreadcrumb()
//   },
//   data () {
//     return {
//       // 页面标题
//       title: '',
//       // 路由集合
//       breadList: ''
//     }
//   },
//   props: ['separtor'],
//   methods: {
//     getBreadcrumb () {
//       this.breadList = this.$route.methods
//       this.$route.matched.forEash((item, index) => {
//         // 判断父级路由是否为空字符串或者meta是否为首页，直接复写路径到根目录
//         // 后面的就是判断路由和当前遍历的项目是否一致，是的话把标题的值给上
//         item.meta.breadcrumbName === '首页' ? item.path = '/'
//           : this.$route.path === item.path ? this.title = item.meta.breadcrumbName : ''
//       })
//     }
//   },
//   watch: {
//     $route () {
//       this.getBreadcrumb()
//     }
//   }
}
</script>