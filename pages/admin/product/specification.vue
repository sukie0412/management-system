<style>
.spe-panel1{
  background-color: #EDEDED;
  height: 80px;
  border-radius: 5px
}
.spe-panel2{
  background-color: #EDEDED;
  height: 100%;
  border-radius: 5px;
  margin-top: 50px;
}
.el-form{
  margin-top:20px;
}
.spe-button{
  margin-left: 50px;
  margin-top: 20px;
}
.spe-table{
  margin-left: 1%;
  margin-top: 10px;
}
</style>
<template>
    <section>
      <div class='spe-panel1'>
        <el-form label-width='120px'>
          <el-row :gutter='10'>
            <el-col :span='3' class='spe-button'>
                <el-button type='primary' icon='el-icon-circle-plus-outline'>添加规格</el-button>
            </el-col>
          </el-row>
        </el-form>
      </div>

      <!-- 列表面板 -->
      <div class='spe-panel2'>
        <el-row>
          <el-table class='spe-table' :data='speData' height='400' border style='width:98%'>
            <el-table-column prop='name' label='规格编号' width='150'></el-table-column>
            <el-table-column prop='name' label='规格名称' width='300'></el-table-column>
            <el-table-column prop='name' label='规格值' width='300'></el-table-column>
            <el-table-column prop='name' label='添加时间' width='250'></el-table-column>
            <el-table-column prop='name' label='更新时间' width='250'></el-table-column>
            <el-table-column prop='name' label='操作' width='280'>
              <template slot-scope="scope">
                <el-button size="mini">编辑</el-button>
                <el-button size="mini">删除</el-button>
<!--                  <el-button size="mini" @click="handleEdit(scope.$index, scope.row)">编辑</el-button>
                <el-button size="mini" type="danger" @click="handleDelete(scope.$index, scope.row)">删除</el-button> -->
              </template>
            </el-table-column>
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