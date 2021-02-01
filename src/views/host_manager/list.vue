<template>
  <el-table
    :data="tableData"
    stripe
    border
    style="width: 100%"
    size="mini"
    highlight-current-row
  >
    <el-table-column type="selection" width="55"> </el-table-column>
    <el-table-column fixed type="index" label="序号" width="50" align="center">
    </el-table-column>
    <el-table-column prop="date" label="日期" width="150"> </el-table-column>
    <el-table-column prop="name" label="姓名" width="120"> </el-table-column>
    <el-table-column prop="province" label="省份" width="120">
    </el-table-column>
    <el-table-column prop="city" label="市区" width="120"> </el-table-column>
    <el-table-column prop="address" label="地址" width="300"> </el-table-column>
    <el-table-column prop="zip" label="邮编" width="120"> </el-table-column>
    <el-table-column prop="age" label="年龄" width="120" align="center">
    </el-table-column>
    <el-table-column prop="sex" label="性别" width="120" align="center">
    </el-table-column>
    <el-table-column prop="height" label="身高" width="120"> </el-table-column>
    <el-table-column prop="weight" label="体重" width="120"> </el-table-column>
    <el-table-column prop="tel" label="联系电话" width="120"> </el-table-column>
    <el-table-column prop="qq" label="QQ" width="120"> </el-table-column>
    <el-table-column prop="wechat" label="微信" width="120"> </el-table-column>
    <el-table-column fixed="right" label="操作" width="250" align="center">
      <template slot-scope="scope">
        <el-button @click="handleClick(scope.row)" size="mini">查看</el-button>
        <el-button type="primary" size="mini">编辑</el-button>
        <el-button type="danger" size="mini">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
</template>

<script>
export default {
  methods: {
    handleClick(row) {
      console.log(row);
    },
  },

  data() {
    return {
      tableData: [
        {
          date: "2016-05-02",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          date: "2016-05-04",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1517 弄",
          zip: 200333,
        },
        {
          date: "2016-05-01",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1519 弄",
          zip: 200333,
        },
        {
          date: "2016-05-03",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1516 弄",
          zip: 200333,
        },
      ],
    };
  },
};
</script>