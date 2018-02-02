<style>
.department-panel1{
  background-color: #EDEDED;
  height: 80px;
  border-radius: 5px
}
.department-panel2{
  background-color: #EDEDED;
  height: 100%;
  border-radius: 5px;
  margin-top: 50px;
}
.department-form{
  margin-top:20px;
}
.dep-button{
  margin-left: 50px;
  margin-top: 20px;
}
.dep-search{
  margin-left:500px;
  margin-top: -40px;
}
.department-table{
  margin-left: 1%;
  margin-top: 10px;
}

</style>

<template>
    <section>
      <div class='department-panel1'>
        <el-form label-width='120px'  :model='form' class='department-form'>
          <el-row :gutter='10'>
            <el-col :span='1' class='dep-button'>
                <el-button type='primary' icon='el-icon-plus'>添加</el-button>
            </el-col>
            <el-col :span='1' class='dep-button'>
                <el-button type='primary' icon='el-icon-edit'>修改</el-button>
            </el-col>
            <el-col :span='2' class='dep-button'>
                <el-button type='danger' icon='el-icon-minus'>删除</el-button>
            </el-col>            
        </el-row>

          <el-form :inline="true" class='dep-search'>
            <el-form-item>
              <el-input v-model="form.departmentName"></el-input>
            </el-form-item>
            <el-form-item>
              <el-button type="primary">部门搜索</el-button>
            </el-form-item>
          </el-form>
        </el-form>
      </div>

      <!-- 列表面板 -->
      <div class='department-panel2'>
        <el-row>
          <el-table class='department-table' :data='departmentData' height='400' border style='width:98%'>
            <el-table-column prop='name' label='部门编号' width='120'></el-table-column>
            <el-table-column prop='name' label='部门名称' width='180'></el-table-column>
            <el-table-column prop='name' label='部门负责人' width='180'></el-table-column>
            <el-table-column prop='name' label='部门职责' width='200'></el-table-column>
            <el-table-column prop='name' label='创建时间' width='200'></el-table-column>
            <el-table-column prop='name' label='更新时间' width='200'></el-table-column>
            <el-table-column prop='name' label='操作' width='220'></el-table-column>
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
          form: {
            departmentName: ''
          }
        }
      }
    }
</script>