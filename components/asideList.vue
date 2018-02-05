<template>
    <!-- 侧边 -->
         <el-aside :isFullScreen="isFullScreen">
            <el-menu background-color="#374049" text-color="#cecece" active-text-color="#4e78d1" :router='true' :unique-opened='true' :default-active='$route.path'>
                <el-submenu index='1'>
                    <template slot='title'><i class="el-icon-setting"> 用户管理</i></template>
                    <el-menu-item index='/admin/system/administrators'>管理员列表</el-menu-item>
                    <el-menu-item index='/admin/system/department'>部门列表</el-menu-item>
                    <el-menu-item index='/admin/system/auth'>权限列表</el-menu-item>
                    <el-menu-item index='1-4'>部门列表</el-menu-item>
                </el-submenu>
                <el-submenu index='2'>
                    <template slot='title'><i class="el-icon-setting"> 订单管理</i></template>
                    <el-menu-item index='/admin/order/orderList'>订单列表</el-menu-item>
                    <el-menu-item index='2-2'>部门列表</el-menu-item>
                    <el-menu-item index='2-3'>部门列表</el-menu-item>
                    <el-menu-item index='2-4'>部门列表</el-menu-item>
                </el-submenu>
                <el-submenu index='3'>
                    <template slot='title'><i class="el-icon-setting"> 产品管理</i></template>
                    <el-menu-item index='/admin/product/product-list'>产品列表</el-menu-item>
                    <el-menu-item index='/admin/product/specification'>规模列表</el-menu-item>
                    <el-menu-item index='3-3'>部门列表</el-menu-item>
                    <el-menu-item index='3-4'>部门列表</el-menu-item>
                </el-submenu>
                <el-submenu index='4'>
                    <template slot='title'><i class="el-icon-setting"> 货运管理</i></template>
                    <el-menu-item index='/admin/transport/transport-list'>货运列表</el-menu-item>
                </el-submenu>
                <el-submenu index='5'>
                    <template slot='title'><i class="el-icon-setting"> 用户管理</i></template>
                    <el-menu-item index='5-1'>部门列表</el-menu-item>
                    <el-menu-item index='5-2'>部门列表</el-menu-item>
                    <el-menu-item index='5-3'>部门列表</el-menu-item>
                    <el-menu-item index='5-4'>部门列表</el-menu-item>
                </el-submenu>
                <el-submenu index='6'>
                    <template slot='title'><i class="el-icon-setting"> 订单管理</i></template>
                    <el-menu-item index='6-1'>部门列表</el-menu-item>
                    <el-menu-item index='6-2'>部门列表</el-menu-item>
                    <el-menu-item index='6-3'>部门列表</el-menu-item>
                    <el-menu-item index='6-4'>部门列表</el-menu-item>
                </el-submenu>
                <el-submenu index='7'>
                    <template slot='title'><i class="el-icon-setting"> 用户管理</i></template>
                    <el-menu-item index='7-1'>部门列表</el-menu-item>
                    <el-menu-item index='7-2'>部门列表</el-menu-item>
                    <el-menu-item index='7-3'>部门列表</el-menu-item>
                    <el-menu-item index='7-4'>部门列表</el-menu-item>
                </el-submenu>
                <el-submenu index='8'>
                    <template slot='title'><i class="el-icon-setting"> 订单管理</i></template>
                    <el-menu-item index='8-1'>部门列表</el-menu-item>
                    <el-menu-item index='8-2'>部门列表</el-menu-item>
                    <el-menu-item index='8-3'>部门列表</el-menu-item>
                    <el-menu-item index='8-4'>部门列表</el-menu-item>
                </el-submenu>
                <el-submenu index='9'>
                    <template slot='title'><i class="el-icon-setting"> 系统设置</i></template>
                    <el-menu-item index='9-1'>部门列表</el-menu-item>
                    <el-menu-item index='9-2'>部门列表</el-menu-item>
                    <el-menu-item index='9-3'>部门列表</el-menu-item>
                    <el-menu-item index='9-4'>部门列表</el-menu-item>
                </el-submenu>
            </el-menu>
        </el-aside>   
</template>

<script>
    export default{

    }
</script>

<style>
.el-aside{
    background-color: #374049;
    height: 800px;
    font-size: 13px;
    text-align: left;
}
</style>