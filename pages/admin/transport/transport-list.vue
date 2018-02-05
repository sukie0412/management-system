<style>
.transport-panel1{
  background-color: #EDEDED;
  height: 80px;
  border-radius: 5px
}
.transport-panel2{
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
      <div class='transport-panel1'>
        <el-form label-width='120px'>
          <el-row :gutter='10'>
            <el-col :span='3' class='adm-button'>
                <el-button type='primary' icon='el-icon-plus'>添加货运</el-button>
            </el-col>
            <el-col :span='3' class='adm-button'>
                <el-button type='danger' icon='el-icon-minus'>批量删除</el-button>
            </el-col>
        </el-row>
        </el-form>
      </div>

      <!-- 列表面板 -->
      <div class='admin-panel2'>
        <el-row>
          <el-table class='admin-table' :data='transportData' height='400' border style='width:98%'>
            <el-table-column prop='name' label='货运公司编号' width='200'></el-table-column>
            <el-table-column prop='name' label='货运名称' width='250'></el-table-column>
            <el-table-column prop='name' label='货运类型' width='250'></el-table-column>
            <el-table-column prop='name' label='更新时间' width='250'></el-table-column>
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