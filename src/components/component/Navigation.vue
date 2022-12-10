<style lang='scss' scoped>
.nav {
  .navList {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    .logo {
      display: inline-block;
      width: 84px;
      height: 84px;
      background-color: #00356B;
      border-radius: 42px;
      margin-right: 120px;
    }
    .el-menu-item {
      padding: 0px 34px;
    }
    .el-menu.el-menu--horizontal {
      border-bottom: none;
    }
    .el-menu-item.is-active{
      background: #00356B !important;
      font-size: 18px;
      line-height: 84px;
      height: 84px;
    }
    .el-menu--horizontal>.el-menu-item {
      font-size: 18px;
      line-height: 84px;
      height: 84px;
    }
  }
  .serch{
    display: inline-block;
    margin-left:30px ;
    border: none;
  }
}
</style>
<template>
  <div class="nav">
    <div class="navList">
      <span class="logo"></span>
      <el-menu
        :default-active="$route.path"
        class="el-menu-demo"
        mode="horizontal"
        background-color="#fff"
        text-color="#00356B"
        active-text-color="#fff"
        router
      >
        <el-menu-item class="first-title" index="/" route="/">首页</el-menu-item>
        <el-menu-item class="first-title" index="/achievement" route="/achievement">业绩成果</el-menu-item>
        <el-menu-item class="first-title" index="/work" route="/work">在研工作</el-menu-item>
        <el-menu-item class="first-title" index="/serve" route="/serve">服务咨询</el-menu-item>
        <el-menu-item class="first-title" index="/contactUs" route="/contactUs">联系我们</el-menu-item>
      </el-menu>
      <el-button class="serch" icon="el-icon-search"></el-button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navigation",
  data() {
    return {
      input2: ""
    };
  },
  methods: {}
};
</script>
