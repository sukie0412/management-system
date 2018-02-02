<style>
.auth-panel1{
  background-color: #EDEDED;
  height: 80px;
  border-radius: 5px
}
.auth-panel2{
  background-color: #EDEDED;
  height: 100%;
  border-radius: 5px;
  margin-top: 50px;
}
.el-form{
  margin-top:20px;
}
.auth-button{
  margin-left: 50px;
  margin-top: 20px;
}
.auth-table{
  margin-left: 1%;
  margin-top: 10px;
}
</style>
<template>
    <section>
      <div class='auth-panel1'>
        <el-form label-width='120px'>
          <el-row :gutter='10'>
            <el-col :span='3' class='auth-button'>
                <el-button type='primary' icon='el-icon-plus'>新增权限</el-button>
            </el-col>
            <el-col :span='3'>
                <el-button type='danger' icon='el-icon-minus'>删除权限</el-button>
            </el-col>
        </el-row>
        </el-form>
      </div>

      <!-- 列表面板 -->
      <div class='auth-panel2'>
        <el-row>
          <el-table class='auth-table' :data='authData' height='400' border style='width:98%'>
            <el-table-column prop='name' label='权限编号' width='120'></el-table-column>
            <el-table-column prop='name' label='权限类型' width='180'></el-table-column>
            <el-table-column prop='name' label='权限名称' width='180'></el-table-column>
            <el-table-column prop='name' label='权限接口' width='200'></el-table-column>
            <el-table-column prop='name' label='创建时间' width='180'></el-table-column>
            <el-table-column prop='name' label='更新时间' width='180'></el-table-column>
            <el-table-column prop='name' label='操作' width='250'></el-table-column>
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