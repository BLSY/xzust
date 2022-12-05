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
        <h3 class="h-text">西藏农牧学院水利水电工程</h3>
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
        <div class="team-text">
          文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文
          字文字文文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文
          字文字文字文字文字字
        </div>
        
      </div>
    </div>
     <div class="cooperation">
      <div class="cooperation-left">
        <div class="line"></div>
        <h3 class="cooperation-title">合作单位</h3>
        <div class="cooperation-icon">About</div>
      </div>
      <div class="cooperation-right">
        <div class="cooperation-text">
          文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文
          字文字文文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文
          字文字文字文字文字字
        </div>
        
      </div>
    </div>
    <div class="preject">
      <div class="carousel">
         <el-carousel :interval="5000" arrow="always" height="425px">
          <el-carousel-item v-for="(item,index) in imgList" :key="index">
            <img :src="item.idView"  class="image">
          </el-carousel-item>
        </el-carousel>
      </div>
      
    </div>
    <div class="group">
      <h3 class="group-title">课题组成员</h3>
      <div class="showMessage" >
        <div class="show-item" v-for="(item,index) in groupList" :key="index">
          <el-image
            style="width: 236px; height: 236px"
            :src="item.imgs"
            :fit="fit"></el-image>
            <h3 class="show-name">{{item.name}}</h3>
            <div class="show-detile">
              {{item.detail}}
            </div>
            <div class="show-icon">
              <div class="icon-circle">
                <i class="el-icon-phone"></i>
              </div>
              <div class="icon-circle">
                <i class="el-icon-message"> </i>
              </div>
            </div>
        </div>
      </div>
    </div>
    <div class="edition">
      <div class="edition-top">
        <div class="edition-logo">
        <h3 class="logo-botton">LOGE</h3>
        <div class="edition-phone">
          <i class="el-icon-phone phone-icon">0000-00000000</i>
          <i class="el-icon-map-location phone-icon">西藏自治区林芝市巴宜区育才西路100号</i>
        </div>
      </div>
      </div>
      <div class="edition-bottom"></div>
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
      imgList:[
        {idView:require('../assets/preject.jpg')},
        {idView:require('../assets/black-preject.jpg')},
        {idView:require('../assets/topbackg.jpg')}
      ],
      groupList:[
        {imgs: require('../assets/preject.jpg'),name:'XXX',detail:'文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本'},
        {imgs: require('../assets/preject.jpg'),name:'XXX',detail:'文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本'},
        {imgs: require('../assets/preject.jpg'),name:'XXX',detail:'文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本'},
        {imgs: require('../assets/preject.jpg'),name:'XXX',detail:'文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本'},
        {imgs: require('../assets/preject.jpg'),name:'XXX',detail:'文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本'},
        {imgs: require('../assets/preject.jpg'),name:'XXX',detail:'文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本'},
        {imgs: require('../assets/preject.jpg'),name:'XXX',detail:'文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本'},
        {imgs: require('../assets/preject.jpg'),name:'XXX',detail:'文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本'}
        ]
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
  box-sizing: border-box;
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
  display: flex;
  align-items: center;
  justify-content: center;
  /* text-align: center; */
  overflow: hidden;
  padding: 0 200px;
}
  .toptext{
    display: inline-block;
    margin-top: 20px;
    width: 70%;
    text-align: left;
  }
  .h-text{
    display: inline-block;
    color: #00356B;
    font-size: 3em;
    letter-spacing:20px;
  }
  .detil{
    margin-top: 20px;
    display: inline-block;
    width:70%;
    font-size: 1em;
    text-align: left;
    letter-spacing: 0.5em;
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
    height: 366px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    padding: 0 200px;
  }
  .team-left{
    height: 250px;
    flex: 1;
    text-align: cente;
    display: inline-block;
    vertical-align: top;
  }
  .team-right{
    height: 250px;
    flex: 1;
    display: inline-block;
    vertical-align: top;
  }
  .team-text{
    text-align: left;
   letter-spacing:0.5em;
   line-height: 2em;
  }
  .team-title{
    color: #00356B;
    font-size: 3em;
    letter-spacing:2em;
    margin: 40px 0;
  }
  .line{
    display: inline-block;
    margin: auto;
    width: 80%;
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
  .cooperation{
    height: 366px;
    display: flex;
    background:#00838F ;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    padding: 0 200px;
  }
   .cooperation-left{
    height: 250px;
    flex: 1;
    text-align: cente;
    display: inline-block;
    vertical-align: top;
  }
  .cooperation-right{
    height: 250px;
    flex: 1;
    display: inline-block;
    vertical-align: top;
  }
  .cooperation-text{
    text-align: left;
   letter-spacing:0.5em;
   line-height: 2em;
   color: #fff;
  }
  .cooperation-title{
    color: #000;
    font-size: 3em;
    letter-spacing:2em;
    margin: 40px 0;
  }
 
  .cooperation-icon{
    text-align: center;
    width: 104px;
    height: 50px;
    line-height: 50px;
    color: #fff;
    font-size: 1em;
    background: #000000;
    border-radius: 25px;
  }
.preject{
  /* height: 366px; */
  display: flex;
  justify-content: center;
  flex-direction: row;
  align-items: center;
  padding: 0 200px;
}
.carousel{
  margin: 88px auto;
  height: 425px;
  width: 90%;
}
/* 轮播图无图片样式 有图片可删除 */
 
  .image{
    width: 100%;
    height: inherit;
  }
  .group{
    text-align: center;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    padding: 0 200px;

  }
  .group-title{
    color: #000;
    font-size: 2em;
    letter-spacing:2em;
    margin: 20px 0;
  }
  .showMessage{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
  }
  .show-item{
    width: 23%;
    display: inline-block;
    margin-bottom: 25px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .show-name{
    color: #000;
    font-size: 1.5em;
    letter-spacing:1em;
  }
  .show-detile{
    width: 236px;
    display: inline-block;
    max-height: 70px;;
    overflow: hidden;
    text-overflow: ellipsis;
    font-size: 1em;
    letter-spacing:0.25em;
    margin: 10px 0;
    display: -webkit-box;
    -webkit-line-clamp: 3;
   -webkit-box-orient: vertical;
  }
  .show-icon{
  }
  .icon-circle{
    margin: 0 10px;
    padding: 5px;
    font-size: 1em;
    border: 1px solid #000;
    border-radius: 1em;
    display: inline-block;
  }
  .edition{
    width: 100%;
    display: flex;
    flex-direction: column;
  }
  .edition-top{
    padding: 0 200px;
    height: 240px;
    color: #FFF;
    background: #383838 ;
  }
  .edition-logo{
    width: 320px;
  }
  .logo-botton{
     color: #FFF;
    font-size: 2em;
    letter-spacing:2em;
    margin: 20px 0;
  }
  .edition-bottom{
    width: 100%;
    height: 60px;
    background: #000000;
  }
</style>
