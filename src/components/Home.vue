<template>
  <div class="indexBox">
    <Navigation />
    <Banner />
    <div class="team">
      <div class="team-box">
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
    </div>
     <div class="cooperation">
       <div class="cooperation-box">
         
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
    <Footer />
  </div>
</template>

<script>
import Navigation from './component/Navigation';
import Banner from './component/Banner';
import Footer from './component/Footer';
export default {
  components: { Navigation, Banner, Footer, },
  name: "Home",
  data() {
    return {
      fit:'',
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
  methods: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
*{
  
  list-style: none;
  box-sizing: border-box;
}
body{
  margin:0;
  padding: 0;
}
html{
  font-size: 16px;
}
.el-menu-demo{
  height: 60px;
}
.first-title{
  font-size: 20px !important;
 
}
.first-title >>>.el-dropdown-menu__item, .el-menu-item{
   padding-left: 32px;
  padding-right: 32px;
  border: 0;
}
.first-title>>>.el-submenu__title{
  font-size: 20px !important;
  padding-left: 32px;
  padding-right: 32px;
}
.top{
  box-sizing: border-box;
  background: url(../assets/topbackg.jpg) no-repeat;
  background-size:100% 100% ;
  position: relative;
  height: 677px;
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
    justify-content: center;
    padding: 0 200px;
  }
  .team-box{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 90%;
  }
  .team-left{
    height: 280px;
    flex: 1;
    text-align: cente;
    display: inline-block;
    vertical-align: top;
  }
  .team-right{
    height: 280px;
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
    letter-spacing:1.5em;
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
    justify-content: center;
    padding: 0 200px;
  }
  .cooperation-box{
    
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 90%;
  }
   .cooperation-left{
    height: 280px;
    flex: 1;
    text-align: cente;
    display: inline-block;
    vertical-align: top;
  }
  .cooperation-right{
    height: 280px;
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
    letter-spacing:1.5em;
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
    width: 90%;
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
    color: #00356B;
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
  .icon-circle{
    width: 30px;
    height: 30px;
    margin: 0 10px;
    padding: 5px;
    font-size: 1em;
    border: 1px solid #000;
    border-radius: 25px;
    display: inline-block;
  }
  
</style>
