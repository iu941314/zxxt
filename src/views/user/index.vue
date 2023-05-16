<template>
  <div>
  <el-card id="search">
    <el-col :span="20">
      <el-input placeholder="用户名"></el-input>
      <el-input placeholder="角色"></el-input>
      <el-button type="primary" icon="el-icon-search">查询</el-button>
    </el-col>
    <el-col :span="4" align="right"></el-col>
    <el-button type="primary" icon="el-icon-circle-plus-outline">新增</el-button>
  </el-card>
  <!--结果列表-->
  <el-card>
    <el-table
      :data="tableData"
      style="width: 100%"
      :row-class-name="tableRowClassName">
      <el-table-column
        prop="date"
        label="日期"
        width="180">
      </el-table-column>
      <el-table-column
        prop="name"
        label="姓名"
        width="180">
      </el-table-column>
      <el-table-column
        prop="address"
        label="地址">
      </el-table-column>
    </el-table>
  </el-card>
<!--    分页插件-->
    <el-pagination
      @size-change="handleSizeChange"
      @current-change="handleCurrentChange"
      :current-page="currentPage4"
      :page-sizes="[10, 20, 50, 100]"
      :page-size="100"
      layout="total, sizes, prev, pager, next, jumper"
      :total="400">
    </el-pagination>
  </div>

</template>

<script>

export default {}
</script>

<style>
#search .el-input {
  width: 200px;
  margin-right: 20px;
}

</style>
