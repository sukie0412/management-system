<template>
<!-- 	<el-breadcrumb-item class='breadcrumbInner'>首页</el-breadcrumb-item>
      <el-breadcrumb-item v-for='item in breadList' :key='item.id' :to='{index:item.index}'>{{tiem.name}}
      </el-breadcrumb-item>
      <el-breadcrumb-item >
        <span>ff</span>
      </el-breadcrumb-item> -->
<!--         <span class="breadcrumb__item">
    <span class="breadcrumb__item__inner" ref="link"><slot></slot></span><span class="breadcrumb__separator">{{separator}}</span>
  </span> -->
  <el-breadcrumb-item :to="{path:'/'}">首页</el-breadcrumb-item>
  <el-breadcrumb-item>用户管理</el-breadcrumb-item>
  <el-breadcrumb-item>部门列表</el-breadcrumb-item>
</template>

<script>
	// export default{
	//   prop: {
	//     to: {},
	//     replace: Boolean
	//   }
	// }
	export default {
//    name: 'ddvuiBreadcrumbItem',
  props: {
    to: {},
    replace: Boolean
  },
  data () {
    return {
      separator: ''
    }
  },
  mounted () {
    this.separator = this.$parent.separator
    var self = this
    if (this.to) {
      let link = this.$refs.link
      link.addEventListener('click', _ => {
        let to = this.to
        self.replace ? self.$router.replace(to)
          : self.$router.push(to)
      })
    }
  }
}
</script>