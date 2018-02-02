<style>
.admin-panel1{
  background-color: #EDEDED;
  height: 80px;
  border-radius: 5px
}
.admin-panel2{
  background-color: #EDEDED;
  height: 100%;
  border-radius: 5px;
  margin-top: 50px;
}
.el-form{
  margin-top:20px;
}
.adm-button{
  margin-left: 50px;
  margin-top: 20px;
}
.admin-table{
  margin-left: 1%;
  margin-top: 10px;
}
</style>
<template>
    <section>
      <div class='admin-panel1'>
        <el-form label-width='120px'>
          <el-row :gutter='10'>
            <el-col :span='3' class='adm-button'>
                <el-button type='primary' icon='el-icon-plus'>添加管理员</el-button>
            </el-col>
            <el-col :span='3' class='adm-button'>
                <el-button type='danger' icon='el-icon-minus'>删除管理员</el-button>
            </el-col>
        </el-row>
        </el-form>
      </div>

      <!-- 列表面板 -->
      <div class='admin-panel2'>
        <el-row>
          <el-table class='admin-table' :data='adminData' height='400' border style='width:98%'>
            <el-table-column prop='name' label='用户编号' width='100'></el-table-column>
            <el-table-column prop='name' label='用户名' width='150'></el-table-column>
            <el-table-column prop='name' label='真实姓名' width='150'></el-table-column>
            <el-table-column prop='name' label='部门' width='150'></el-table-column>
            <el-table-column prop='name' label='角色' width='100'></el-table-column>
            <el-table-column prop='name' label='账号状态' width='100'></el-table-column>
            <el-table-column prop='name' label='创建时间' width='180'></el-table-column>
            <el-table-column prop='name' label='更新时间' width='180'></el-table-column>
            <el-table-column prop='name' label='操作' width='200'></el-table-column>
          </el-table>
        </el-row>
      </div>
    </section>
</template>

<script>
    export default{
      layout: 'admin',
      data () {
        return {
    
        }
      }
    }
</script>