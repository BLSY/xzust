<style lang="scss">
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
                    margin-bottom: 25px;
                }
                .form {
                    .el-form-item {
                        position: relative;
                    }
                    .el-form-item__label {
                        text-align: left;
                        padding: 0px 0px 0px 40px;
                    }
                    .el-form-item::before {
                        display: inline-block;
                        width: 8px;
                        height: 8px;
                        background-color: #00356B;
                        border-radius: 4px;
                        position: absolute;
                        top: 20px;
                        left: 2%;
                        z-index: 9;
                        transform: translate(0, -50%);
                    }
                    .el-input {
                        width: 70%;
                    }
                    .el-textarea {
                        width: 70%;
                    }
                }
                .upList {
                    p {
                        display: flex;
                        justify-content: space-between;
                        position: relative;
                        line-height: 40px;
                    }
                    .name {
                        position: relative;
                        padding-left: 20px;
                    }
                    p::before {
                        display: inline-block;
                        width: 10px;
                        height: 10px;
                        border-radius: 5px;
                        background-color: #00356B;
                        position: absolute;
                        content: "";
                        top: 50%;
                        transform: translateY(-50%);
                    }
                }
            }
        }
    }
    .show {
        display: block;
    }
    .noShow {
        display: none;
    }
}
</style>
<template>
    <div class="serve">
        <Navigation />
        <div :class="[banner ? 'show' : 'noShow']"><Banner /></div>
        <div class="serveContent">
            <div class="littleNav">
                <el-breadcrumb separator-class="el-icon-arrow-right">
                    <el-breadcrumb-item><i class="el-icon-s-home" style="margin-right: 10px"></i>?????????????????????</el-breadcrumb-item>
                    <el-breadcrumb-item>????????????</el-breadcrumb-item>
                    <el-breadcrumb-item>{{curTitle}}</el-breadcrumb-item>
                </el-breadcrumb>
            </div>
            <div class="content">
                 <div class="left">
                    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="vetical"
                        background-color="#F7F7F7" text-color="#444" active-text-color="#fff"
                        @select="handleSelect"
                        >
                        <el-menu-item class="left_title" index="consult">????????????</el-menu-item>
                        <el-menu-item class="left_title" index="download">????????????</el-menu-item>
                    </el-menu>
                 </div>
                 <div class="right">
                    <div class="right_title">{{curTitle}}</div>
                    <div :class="[activeIndex === 'consult' ? 'show': 'noShow']">
                        <div class="form">
                            <el-form ref="ruleForm" label-width="160px" class="demo-ruleForm">
                                <el-form-item label="??????">
                                    <el-input></el-input>
                                </el-form-item>
                                <el-form-item label="????????????" prop="mail">
                                    <el-input></el-input>
                                </el-form-item>
                                <el-form-item label="????????????" prop="phone">
                                    <el-input></el-input>
                                </el-form-item>
                                <el-form-item label="?????????????????????">
                                    <el-input></el-input>
                                </el-form-item>
                                <el-form-item label="????????????">
                                    <el-input></el-input>
                                </el-form-item>
                                <el-form-item label="??????">
                                    <el-input></el-input>
                                </el-form-item>
                                <el-form-item label="???????????????" prop="desc">
                                    <el-input type="textarea"></el-input>
                                </el-form-item>
                            </el-form>
                        </div>
                    </div>
                    <div :class="[activeIndex === 'download' ? 'show': 'noShow']">
                        <div class="upList" v-for="(item, index) in upList" :key="index">
                            <p>
                                <span class="name">{{item.name}}</span>
                                <span class="time">{{item.time}}</span>
                            </p>
                        </div>
                    </div>
                 </div>
            </div>
        </div>
        <Footer />
    </div>
</template>

<script>
import Navigation from './component/Navigation'
import Footer from './component/Footer'
import Banner from './component/Banner'

export default {
    components: { Navigation, Footer, Banner, },
    data() {
        return {
            activeIndex: "consult",
            curTitle: '????????????',
            banner: true,
            upList: [
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
                { name: '???????????????????????????????????????????????????????????????', time: '(2020.1.29)'},
            ]
        }
    },
    methods: {
        handleSelect(key, keyPath) {
            switch(key) {
                case 'download' :
                    this.curTitle = '????????????'
                    this.activeIndex = 'download'
                    this.banner = false
                break;
                case 'consult' :
                    this.curTitle = '????????????'
                    this.activeIndex = 'consult'
                    this.banner = true
                break;
            }
        }
    }
}
</script>