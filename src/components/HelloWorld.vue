<template>
  <div>
    <el-card class="box-card">
      <div slot="header" class="clearfix">
        <span style="font-size: 22px"
          >哈喽呀，各位小可爱，快选出你认为是五大基本地形的选项吧！</span
        >
      </div>
      <div>
        <el-checkbox
          class="aaa"
          v-model="checked0"
          label="冰川"
          border
        ></el-checkbox>
        <el-checkbox
          class="aaa"
          v-model="checked1"
          label="平原"
          border
        ></el-checkbox
        ><br />
        <el-checkbox
          class="aaa"
          v-model="checked2"
          label="沙漠"
          border
        ></el-checkbox>
        <el-checkbox
          class="aaa"
          v-model="checked3"
          label="盆地"
          border
        ></el-checkbox
        ><br />
        <el-checkbox
          class="aaa"
          v-model="checked4"
          label="湿地"
          border
        ></el-checkbox>
        <el-checkbox
          class="aaa"
          v-model="checked5"
          label="湖泊"
          border
        ></el-checkbox
        ><br />
        <el-checkbox
          class="aaa"
          v-model="checked6"
          label="丘陵"
          border
        ></el-checkbox>
        <el-checkbox
          class="aaa"
          v-model="checked7"
          label="高原"
          border
        ></el-checkbox
        ><br />
        <el-checkbox
          class="aaa"
          v-model="checked8"
          label="峡谷"
          border
        ></el-checkbox>
        <el-checkbox
          class="aaa"
          v-model="checked9"
          label="山地"
          border
        ></el-checkbox
        ><br />
        <el-checkbox
          class="aaa"
          v-show="false"
          label="峡谷"
          border
        ></el-checkbox>
        <el-checkbox
          class="aaa"
          v-show="false"
          label="峡谷"
          border
        ></el-checkbox>
      </div>
      <div>
        <el-button type="primary" style="margin-top: 10px" @click="commit()"
          >提交结果</el-button
        >
      </div>
    </el-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
      checked0: false,
      checked1: false,
      checked2: false,
      checked3: false,
      checked4: false,
      checked5: false,
      checked6: false,
      checked7: false,
      checked8: false,
      checked9: false,
    };
  },
  methods: {
    commit() {
      //1 3 6 7 9
      if (
        this.checked0 == false &&
        this.checked1 == true &&
        this.checked2 == false &&
        this.checked3 == true &&
        this.checked4 == false &&
        this.checked5 == false &&
        this.checked6 == true &&
        this.checked7 == true &&
        this.checked8 == false &&
        this.checked9 == true
      ) {
        this.$message({
          showClose: true,
          duration: 0,
          message: "太棒啦，恭喜你，答案全部正确！",
          type: "success",
        });
      } else {
        this.$message({
          showClose: true,
          duration: 0,
          message: "有点小问题哟！快看看正确答案吧！",
          type: "warning",
        });
      }
      //显示正确答案
      this.checked0 = false;
      this.checked1 = true;
      this.checked2 = false;
      this.checked3 = true;
      this.checked4 = false;
      this.checked5 = false;
      this.checked6 = true;
      this.checked7 = true;
      this.checked8 = false;
      this.checked9 = true;
    },
  },
};
</script>
<style>
.aaa {
  margin: 5px;
}
.text {
  font-size: 14px;
}

.item {
  margin-bottom: 18px;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}
.clearfix:after {
  clear: both;
}

.box-card {
  width: 680px;
  /* text-align: center; */
  margin-left: auto;
  margin-right: auto;
  margin-top: 60px;
}
</style>
