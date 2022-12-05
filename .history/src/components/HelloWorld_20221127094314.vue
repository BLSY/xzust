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
    <div class="top">
      <div class="toptext">
        <h3 class="h-text">西藏农牧学院水利工程</h3>
        <h3 class="h-text" >郭永刚老师课题组</h3>
        <div class="detil">
          文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
        </div>
        
      </div>
      <div class="starvidio">
        </div>
    </div>
    <div class="team">
      <div class="team-left">
        <div class="line"></div>
        <h3 class="team-title">团队简介</h3>
        <div class="team-icon">About</div>
      </div>
      <div class="team-right">
        <div class="right-text">
          文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文
          字文字文文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文
          字文字文字文字文字字
        </div>
        
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
*{
  list-style: none;
}
h3{
  margin: 0;
  padding: 0;
  margin: 10px 0;
}
html{
  font-size: 16px;
}
.indexBox {
  width: 100%;
  height: 100%;
  position: relative;
  box-sizing: border-box;
}
.nav {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 200px;
}
.login {
  flex: 1;
  display: inline-block;
  font-size: 3em;
  font-weight: bold;
  color: #00356B;
  font-family: MicrosoftYaHei;
  margin-right: 100px;
}
.navList{
  flex: 4;
  display: inline-block;
  min-width:55%;
  font-size: 2em;
}
.serch{
  flex: 1;
  display: inline-block;
  margin-left:30px ;
}
.el-menu-item.is-active{
  background: #00356B !important;
}
.top{
  box-sizing: border-box;
  background: url(../assets/topbackg.jpg) no-repeat;
  background-size:100% 100% ;
  position: relative;
  height: 500px;
  text-align: center;
  overflow: hidden;
  padding: 0 200px;
}
  .toptext{
    display: inline-block;
    margin-top: 20px;
    text-align: left;
  }
  .h-text{
    color: #00356B;
    font-size: 3em;
    letter-spacing:20px;
  }
  .detil{
    display: inline-block;
    width:300px;
    font-size: 1em;
    text-align: left;
    color:#333;
  }
  .starvidio{
    background: url(../assets/bapfang.png) no-repeat;
    background-size:100% 100% ;
    position: absolute;
    bottom: 20px;
    right: 60px;
    height: 60px;
    width: 60px;
  }
  .team{
    height: 240px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    padding: 0 200px;
  }
  .team-left{
    width: 500px;
    text-align: cente;
  }
  .team-right{
    width: 600px;
  }
  .right-text{
    width: 400px;
    text-align: left;
   letter-spacing:3px;
  }
  .team-title{
    color: #00356B;
    font-size: 40px;
    letter-spacing:20px;
  }
  .line{
    display: inline-block;
    margin: auto;
    width: 233px;
    border: 1px solid #5D0E8B;
  }
  .team-icon{
    text-align: center;
    width: 104px;
    height: 50px;
    line-height: 50px;
    color: #fff;
    font-size: 1em;
    background: #00356B;
    border-radius: 25px;
  }
</style>
