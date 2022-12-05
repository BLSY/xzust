<template>
  <div class="indexBox">
    <div class="nav">
      <div class="login">LOGO</div>
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
          <el-menu-item index="1">首页</el-menu-item>
          <el-submenu index="2">
            <template slot="title">业绩成果</template>
            <el-menu-item index="2-1">选项1</el-menu-item>
            <el-menu-item index="2-2">选项2</el-menu-item>
            <el-menu-item index="2-3">选项3</el-menu-item>
          </el-submenu>
          <el-menu-item index="3">在研工作</el-menu-item>
          <el-menu-item index="4">服务咨询</el-menu-item>
          <el-menu-item index="5">联系我们</el-menu-item>
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
  name: "HelloWorld",
  data() {
    return {
      activeIndex2: "1",
      input2: "",
    };
  },
  props: {
    msg: String,
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
.indexBox {
  width: 100%;
  height: 100%;
  position: relative;
 
  
}
.nav {
  width: 100%;
  display: flex;
  align-items: center;
}
.login {
  display: inline-block;
  font-size: 32px;
  font-weight: bold;
  font-family: MicrosoftYaHei;
  margin-left: 200px;
  margin-right: 100px;
}
.navList{
  width: 60%;
  display: inline-block;
}
.serch{
  display: inline-block;
  margin-left:30px ;
}
/deep/.el-menu-item.is-active{
  background: #00356B;
}
</style>
