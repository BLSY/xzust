<style lang='scss' scoped>
.nav {
  .tabbox {
    padding: 0px 120px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    .logo {
      display: inline-block;
      width: 121px;
      height: 28px;
    }
    .navList {
      display: inline-block;
      .el-menu.el-menu--horizontal {
        border-bottom: none;
      }
      .el-menu-item.is-active{
        background: #00356B !important;
      }
    }
    .serch{
      display: inline-block;
      margin-left:30px ;
      min-width: 120px;
    }
  }
}
</style>
<template>
  <div class="nav">
    <div class="tabbox">
      <img class="logo" src="../../assets/img/logo.png" alt="" />
      <div class="navList">
        <el-menu
          :default-active="activeIndex2"
          class="el-menu-demo"
          mode="horizontal"
          @select="handleSelect"
          background-color="#fff"
          text-color="#00356B"
          active-text-color="#fff"
        >
          <el-menu-item index="/" class="first-title">首页</el-menu-item>
          <el-menu-item class="first-title" index="/achievement">业绩成果</el-menu-item>
          <!-- <el-submenu index="/achievement" class="first-title">
            <template slot="title" class="first-title">业绩成果</template>
            <el-menu-item index="2-1">选项1</el-menu-item>
            <el-menu-item index="2-2">选项2</el-menu-item>
            <el-menu-item index="2-3">选项3</el-menu-item>
          </el-submenu> -->
          <el-menu-item class="first-title" index="/work">在研工作</el-menu-item>
          <el-menu-item class="first-title" index="/serve">服务咨询</el-menu-item>
          <el-menu-item class="first-title" index="/contactUs">联系我们</el-menu-item>
        </el-menu>
      </div>
      <div class="serch">
        <el-input
          placeholder="请输入内容"
          prefix-icon="el-icon-search"
          v-model="input2"
        >
        </el-input>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navigation",
  data() {
    return {
      activeIndex2: "1",
      input2: ""
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
      this.$router.push(keyPath[0]);
    }
  }
};
</script>
