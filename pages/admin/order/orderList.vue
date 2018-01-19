<style>
.order-panel1{
  background-color: #e9ebec;
  height: 140px;
  border-radius: 10px
}
.order-panel2{
  background-color: #e9ebec;
  height: 400px;
  border-radius: 10px;
  margin-top: 30px;
}
  .el-form{
    margin-top:20px;
  }
  .el-form-item{
    margin-top: 20px;
  }
  .el-button{
    margin-left: 50px;
    margin-bottom: 20px;
  }
  .el-table{
    margin-top: 30px;
    margin-left: 1%;
    margin-right: 1%
  }
  .el-table-column{
    margin-top: 10px;
  }

</style>

<template>
    <section>
      <div class='order-panel1'>
              <!-- 搜索 -->
        <el-form ref='el-form' :model='form' label-width='120px' >
            <el-row :gutter='15'>
              <el-col :span='6'>
                <el-form-item label='商品名称'>
                  <el-input v-model='form.goodsName'></el-input>
                </el-form-item>
              </el-col>

              <el-col :span='6'>
                <el-form-item label='订单编号'>
                  <el-input v-model='form.orderNum'></el-input>
                </el-form-item>
              </el-col>

              <el-col :span='6'>
                <el-form-item label='订单状态'>
                  <el-select v-model='form.orderStatus'>
                    <el-option v-for='item in orderStatus' :key='item.value' :label='item.label' :value='item.value'></el-option>
                  </el-select>
                </el-form-item>
              </el-col>
            </el-row>
            <el-row :gutter='10'>
              <el-col :span='3'>
                <el-button type='primary' icon='el-icon-search'>搜索订单</el-button>
              </el-col>  
              <el-col :span='3'>
                <el-button type='primary' icon='el-icon-upload2'>导出列表</el-button>
              </el-col>
            </el-row>
        </el-form>
      </div>  
      <div class='order-panel2'>
        <!-- 表格 -->
        <el-row>
          <el-table :data='tableData' border style='width:98%'>
            <el-table-column type='selection' width='80'></el-table-column>
            <el-table-column prop='orderId' label='订单ID' width='180'></el-table-column>
            <el-table-column prop='orderNum' label='订单编号' width='180'></el-table-column>
            <el-table-column prop='account' label='账户名' width='160'></el-table-column>
            <el-table-column prop='goodsList' label='产品清单' width='180'></el-table-column>
            <el-table-column prop='orderStatus' label='订单状态' width='100'></el-table-column>
            <el-table-column prop='payType' label='支付方式' width='110'></el-table-column>
            <el-table-column prop='orderMoney' label='订单金额' width='110'></el-table-column>
            <el-table-column prop='remarks' label='备注' width='200'></el-table-column>
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
        goodsName: '',
        orderNum: ''
      },
      orderStatus: [{
        value: 0,
        label: '状态1'
      }, {
        value: 1,
        label: '状态2'
      }, {
        value: 3,
        label: '状态3'
      }]
    }
  }
}
</script>