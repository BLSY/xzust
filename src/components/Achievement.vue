<style lang="scss" scoped>
.achievement {
    .achiveve {
        padding: 34px 334px 68px 334px;
        .content {
            display: flex;
            justify-content: space-between;
            margin-top: 30px;
            .left {
                width: 240px;
                .el-menu {
                    border-right: none;
                }
                .el-menu-item {
                    border-bottom: 1px solid #444;
                }
                .el-menu-item.is-active{
                    background: #00356B !important;
                }
            }
            .right {
                display: inline-block;
                width: 970px;
                .right_title {
                    width: 100%;
                    font-size: 22px;
                    color: #00356B;
                    border-bottom: 1px solid #00356B;
                }
                .show {
                    display: block;
                }
                .noShow {
                    display: none;
                }
            }
        }
    }
}
</style>
<template>
    <div class="achievement">
        <Navigation />
        <Banner />
        <div class="achiveve">
            <div class="littleNav">
                <el-breadcrumb separator-class="el-icon-arrow-right">
                    <el-breadcrumb-item><i class="el-icon-s-home" style="margin-right: 10px"></i>您当前的位置：</el-breadcrumb-item>
                    <el-breadcrumb-item>业绩成果</el-breadcrumb-item>
                    <el-breadcrumb-item>{{curTitle}}</el-breadcrumb-item>
                </el-breadcrumb>
            </div>
            <div class="content">
                 <div class="left">
                    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="vetical"
                        background-color="#F7F7F7" text-color="#444" active-text-color="#fff"
                        @select="handleSelect"
                        >
                        <el-menu-item class="left_title" index="paper">发表论文</el-menu-item>
                        <el-menu-item class="left_title" index="science">科研成果</el-menu-item>
                        <el-menu-item class="left_title" index="software">软件成果</el-menu-item>
                        <el-menu-item class="left_title" index="apparatus">仪器设备</el-menu-item>
                    </el-menu>
                 </div>
                 <div class="right">
                    <div class="right_title">{{curTitle}}</div>
                    <div :class="[activeIndex === 'paper' ? 'show': 'noShow']">发表论文</div>
                    <div :class="[activeIndex === 'science' ? 'show': 'noShow']">科研成果</div>
                    <div :class="[activeIndex === 'software' ? 'show': 'noShow']">软件成果</div>
                    <div :class="[activeIndex === 'apparatus' ? 'show': 'noShow']">仪器设备</div>
                 </div>
            </div>
        </div>
        <Footer />
    </div>
</template>

<script>
import Navigation from './component/Navigation'
import Banner from './component/Banner'
import Footer from './component/Footer'
export default {
    components: { Navigation, Banner, Footer, },
    data() {
        return {
            activeIndex: "paper",
            curTitle: '发表论文',
        }
    },
    methods: {
        handleSelect(key, keyPath) {
            switch(key) {
                case 'paper' :
                    this.curTitle = '发表论文'
                    this.activeIndex = 'paper'
                break;
                case 'science' :
                    this.curTitle = '科研成果'
                    this.activeIndex = 'science'
                break;
                case 'software' :
                    this.curTitle = '软件成果'
                    this.activeIndex = 'software'
                break;
                case 'apparatus' :
                    this.curTitle = '仪器设备'
                    this.activeIndex = 'apparatus'
                break;
            }
        }
  }
}
</script>