<template>
  <div style="padding:20px;box-sizing:border-box;">
    <el-table :data="tableData" style="width: 100%" border>
      <el-table-column prop="name" label="姓名" width="380">
        <template slot-scope="scope">
          <el-input
            type="textarea"
            :autosize="{ minRows: 3, maxRows: 10 }"
            placeholder="请输入"
            v-model="scope.row.name"
            clearable
            resize="both"
            @resize="inputResize"
          >
          </el-input>
        </template>
      </el-table-column>
      <el-table-column prop="address" label="地址" width="380">
        <template slot-scope="scope">
          <el-input
            type="textarea"
            :autosize="{ minRows: 3, maxRows: 10 }"
            placeholder="请输入"
            v-model="scope.row.address"
            clearable
            resize="both"
            @resize="inputResize"
          >
          </el-input>
        </template>
      </el-table-column>
      <el-table-column prop="date" label="日期"> </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tableData: [
        {
          date: "2016-05-02",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1518 弄"
        },
        {
          date: "2016-05-04",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1517 弄"
        },
        {
          date: "2016-05-01",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1519 弄"
        },
        {
          date: "2016-05-03",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1516 弄"
        }
      ]
    };
  }
};
</script>
