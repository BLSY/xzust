<style lang="scss" scoped>
.serve {
    .serveContent {
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
    <div class="serve">
        <Navigation />
        <div class="serveContent">
            <div class="littleNav">
                <el-breadcrumb separator-class="el-icon-arrow-right">
                    <el-breadcrumb-item><i class="el-icon-s-home" style="margin-right: 10px"></i>您当前的位置：</el-breadcrumb-item>
                    <el-breadcrumb-item>服务咨询</el-breadcrumb-item>
                    <el-breadcrumb-item>{{curTitle}}</el-breadcrumb-item>
                </el-breadcrumb>
            </div>
            <div class="content">
                 <div class="left">
                    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="vetical"
                        background-color="#F7F7F7" text-color="#444" active-text-color="#fff"
                        @select="handleSelect"
                        >
                        <el-menu-item class="left_title" index="download">下载中心</el-menu-item>
                        <el-menu-item class="left_title" index="consult">业务咨询</el-menu-item>
                    </el-menu>
                 </div>
                 <div class="right">
                    <div class="right_title">{{curTitle}}</div>
                    <div :class="[activeIndex === 'download' ? 'show': 'noShow']">下载中心</div>
                    <div :class="[activeIndex === 'consult' ? 'show': 'noShow']">业务咨询</div>
                 </div>
            </div>
        </div>
        <Footer />
    </div>
</template>

<script>
import Navigation from './component/Navigation'
import Footer from './component/Footer'
export default {
    components: { Navigation, Footer, },
    data() {
        return {
            activeIndex: "download",
            curTitle: '下载中心',
        }
    },
    methods: {
        handleSelect(key, keyPath) {
            switch(key) {
                case 'download' :
                    this.curTitle = '下载中心'
                    this.activeIndex = 'download'
                break;
                case 'consult' :
                    this.curTitle = '业务咨询'
                    this.activeIndex = 'consult'
                break;
            }
        }
    }
}
</script>