<style lang="scss" scoped>
    .edition{
    width: 100%;
    display: flex;
    flex-direction: column;
  }
  .edition-top{
    padding: 0 200px;
    height: 238px;
    color: #FFF;
    display: flex;
    flex-direction: row;
    background: #383838 ;
    justify-content: center;
  }
  .bottom-boxs{
    width: 90%;
     height: 238px;
    color: #FFF;
    display: flex;
    flex-direction: row;
    padding-left: 27px;
  }
  .edition-logo{
    width: 320px;
  }
  .logo-botton{
    background: #FFF;
    width: 60px;
    height: 60px;
    border-radius: 30px;
    margin: 20px 0;
  }
  /* .el-icon-phone {
    font-size:1.5em;
  } */
  .edition-phone{
     font-size: 1em;
  }
  .edition-phone>.el-icon-phone{
   font-size:1.5em; 
  }

  .el-icon-map-location{
    margin: 10px 0;
     font-size: 1.5em;
  }
  .phone-icon{
    font-size: 1.25em;
    margin: 10px 0;
  }
  .address-icon{
    font-size: 1em;
  }
  .edition-bottom{
    width: 100%;
    height: 53px;
    background: #000000;
  }
  .edition-message{
    margin-left:200px ;
    display: flex;
    flex: 2;
    margin-top: 20px;
    justify-content: center;
  }
  .message-item{
   flex: 1;

  }
  .titles{
    font-size: 1.4em;
    margin: 10px 0;
  }
  .texts{
    font-size: 1em;
    margin: 10px 0;
  }
</style>
<template>
  <div class="footer">
    <div class="edition">
      <div class="edition-top">
        <div class="bottom-boxs">
          <div class="edition-logo">
            <div class="logo-botton"></div>
            <div class="edition-phone">
              <i class="el-icon-phone "></i>
              <span class="phone-icon">0000-00000000</span>
              <br />
              <i class="el-icon-map-location"></i>
              <span class="address-icon">
                西藏自治区林芝市巴宜区育才西路100号</span
              >
            </div>
          </div>
          <div class="edition-message">
            <div class="message-item">
              <div class="titles">联系我们</div>
              <div class="texts">联系电话</div>
              <div class="texts">邮箱</div>
              <div class="texts">微信</div>
            </div>
            <div class="message-item">
              <div class="titles">研发工作</div>
              <div class="texts">软件研发</div>
              <div class="texts">硬件研发</div>
            </div>
            <div class="message-item">
              <div class="titles">业绩成果</div>
              <div class="texts">发表论文</div>
              <div class="texts">科研项目</div>
              <div class="texts">软件成果</div>
              <div class="texts">仪器设备</div>
            </div>
            <div class="message-item">
              <div class="titles">服务咨询</div>
              <div class="texts">下载中心</div>
              <div class="texts">业务咨询</div>
            </div>
          </div>
        </div>
      </div>
      <div class="edition-bottom"></div>
    </div>
  </div>
</template>
