<template>
  <!-- <div class="tree"> -->
  <el-tree
    :data="data"
    show-checkbox
    node-key="id"
    :default-expanded-keys="[2, 3]"
    :default-checked-keys="[9]"
    :props="defaultProps"
  >
  </el-tree>
  <!-- </div> -->
</template>

<script>
export default {
  data() {
    return {
      data: [
        {
          id: 1,
          label: "一级",
          children: [
            {
              id: 4,
              label: "二级 1-1",
              children: [
                {
                  id: 9,
                  label: "三级 1-1-1",
                },
                {
                  id: 10,
                  label: "三级 1-1-2",
                },
              ],
            },
          ],
        },
        {
          id: 2,
          label: "一级 2",
          children: [
            {
              id: 5,
              label: "二级 2-1",
            },
            {
              id: 6,
              label: "二级 2-2",
            },
          ],
        },
        {
          id: 3,
          label: "一级 3",
          children: [
            {
              id: 7,
              label: "二级 3-1",
            },
            {
              id: 8,
              label: "二级 3-2",
            },
          ],
        },
      ],
      data1: [
        {
          id: 1,
          label: "三维模型",
          children: [
            {
              id: 2,
              label: "DAE模型",
              children: [
                {
                  id: 3,
                  label: " ",
                },
                {
                  id: 3,
                  label: " ",
                },
              ],
            },
            {
              id: 2,
              label: "fbx模型",
              children: [
                {
                  id: 3,
                  label: " ",
                },
                {
                  id: 3,
                  label: " ",
                },
              ],
            },
            {
              id: 2,
              label: "glb模型",
              children: [
                {
                  id: 3,
                  label: " ",
                },
                {
                  id: 3,
                  label: " ",
                },
              ],
            },
            {
              id: 2,
              label: "3dtileset模型",
              children: [
                {
                  id: 3,
                  label: " ",
                },
                {
                  id: 3,
                  label: " ",
                },
              ],
            },
          ],
        },
        {
          id: 1,
          label: "矢量数据",
          children: [
            {
              id: 2,
              label: "GeoJSON点",
              children: [
                {
                  id: 3,
                  label: " ",
                },
                {
                  id: 3,
                  label: " ",
                },
              ],
            },
            {
              id: 2,
              label: "GeoJSON线",
              children: [
                {
                  id: 3,
                  label: " ",
                },
                {
                  id: 3,
                  label: " ",
                },
              ],
            },
            {
              id: 2,
              label: "GeoJSON面",
              children: [
                {
                  id: 3,
                  label: " ",
                },
                {
                  id: 3,
                  label: " ",
                },
              ],
            },
          ],
        },
      ],
      methods: {
        // 读取和写入文件,创建树形控件的数据函数
        readOrWriteFile() {
          // 文件系统模块执行文件操作
          // const fs = require('fs');
          // json数据
          // var jsonData = '{"persons":[{"name":"John","city":"New York"},{"name":"Phil","city":"Ohio"}]}';
          // 解析json
          // var jsonObj = JSON.parse(jsonData);
          // console.log(jsonObj);
          // 字符串化JSON对象
          // var jsonContent = JSON.stringify(jsonObj);
          // console.log(jsonContent);
          // fs.writeFile("output.json", jsonContent, 'utf8', function (err) {
          //     if (err) {
          //         console.log("An error occured while writing JSON Object to File.");
          //         return console.log(err);
          //     }
          //     console.log("JSON file has been saved.");
          //  });
        },
      },
      defaultProps: {
        children: "children",
        label: "label",
      },
    };
  },
};
</script>

<style scoped>
div.el-tree {
  position: absolute;
  z-index: 20;
  right: 16px;
  top: 80px;
  color: #fff;
  background-color: rgba(36, 56, 72, 0.9);
}
</style>