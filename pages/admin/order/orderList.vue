<template>
    <section>
        <el-form ref='el-form' :model='form' label-width='300px'>
            <el-form-item label='商品名称'>
                <el-input v-model='form.goodsName'></el-input>
            </el-form-item>
            <el-form-item label='订单编号'>
                <el-input v-model='form.orderNum'></el-input>
            </el-form-item>
            <el-form-item label='订单状态'>
                <el-select v-model='form.orderStatus'>
                  <el-option  v-for='item in orderOptions' :key='item.value' :label='item.label' :value='item.value'></el-option>
                </el-select>
            </el-form-item>
            <div>
                <el-button type='primary' icon='el-icon-search'>搜索订单</el-button>
                <el-button type='primary' icon='el-icon-upload2'>导出列表</el-button>
            </div>
        </el-form>
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