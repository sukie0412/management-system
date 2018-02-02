<style>
.product-panel1{
  background-color: #EDEDED;
  height: 140px;
  border-radius: 5px
}
.product-panel2{
  background-color: #EDEDED;
  height: 100%;
  border-radius: 5px;
  margin-top: 50px;
}
.el-form{
  margin-top:20px;
}
.product-button{
  margin-left: 50px;
  margin-top: 20px;
}
.product-table{
  margin-left: 1%;
  margin-top: 10px;
}
</style>
<template>
    <section>
      <div class='product-panel1'>
        <el-form label-width='120px'>
          <el-row :gutter='10'>
            <el-col :span='3' class='product-button'>
                <el-button type='primary' icon='el-icon-circle-plus-outline'>新增产品</el-button>
            </el-col>
          </el-row>
          <el-row :gutter='10'>
            <el-col :span='2' class='product-button'>
                <el-button type='info' icon='el-icon-sort'>批量上架</el-button>
            </el-col>
            <el-col :span='2' class='product-button'>
                <el-button type='info' icon='el-icon-sort'>批量下架</el-button>
            </el-col>
            <el-col :span='2' class='product-button'>
                <el-button type='danger' icon='el-icon-remove-outline'>批量删除</el-button>
            </el-col>
          </el-row>
        </el-form>

      </div>

      <!-- 列表面板 -->
      <div class='product-panel2'>
        <el-row>
          <el-table class='product-table' :data='productData' height='400' border style='width:98%'>
            <el-table-column prop='name' label='用户编号' width='120'></el-table-column>
            <el-table-column prop='name' label='用户名' width='180'></el-table-column>
            <el-table-column prop='name' label='真实姓名' width='180'></el-table-column>
            <el-table-column prop='name' label='部门' width='180'></el-table-column>
            <el-table-column prop='name' label='角色' width='150'></el-table-column>
            <el-table-column prop='name' label='账号状态' width='140'></el-table-column>
            <el-table-column prop='name' label='创建时间' width='200'></el-table-column>
            <el-table-column prop='name' label='更新时间' width='200'></el-table-column>
            <el-table-column prop='name' label='操作' width='180'>
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