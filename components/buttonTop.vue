<style>
.el-header{
    background-color: #374049;
    color: #cecece;
    line-height: 50px;
}
.headerName,.menuButton{
    text-align: left;
    font-size: 25px;
    margin-right: 110px;
}
.el-header span{
    position:absolute;
    right: 3%;
}
.logout{
    cursor: pointer;
}

</style>

<template>
        <el-header>
            <a class='headerName'>后台管理系统</a>
            <i class='el-icon-menu menuButton'></i>
            <!-- 未登录状态 -->
<!--             <span v-if='!loginStatus'>
                <a class='signIn'>点我注册</a>
                <a class='login' @click="login">已有账号</a>
            </span> -->
            <!-- 登录状态 -->
            <span>
                <a class='user'>xxx，</a>
                <a class='logout' @click="logout">退出</a>
            </span>
        </el-header>
</template>

<script>
export default{
  methods: {
    logout () {
      this.$confirm('是否确认退出？', '提示', {
        type: 'warning'
      })
    }
  }
}
</script>
