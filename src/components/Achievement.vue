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
                    line-height: 42px;
                    border-bottom: 1px solid #00356B;
                    margin-bottom: 31px;
                }
                .simple {
                    display: flex;
                    justify-content: space-between;
                    flex-wrap: wrap;
                    .block {
                        display: inline-block;
                        width: 32%;
                        height: 310px;
                        background-color: #00356B;
                        margin-bottom: 22px;
                        color: #fff;
                        font-size: 33px;
                        text-align: center;
                    }
                    p {
                        width: 100%;
                        line-height: 34px;
                        margin: 0;
                    }
                    .el-pagination {
                        width: 100%;
                        text-align: center;
                        margin-top: 30px;
                        
                    }
                    .el-pagination.is-background .el-pager li:not(.disabled).active {
                        background-color: #00356B !important;
                    }
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
                    <div :class="[activeIndex === 'paper' ? 'simple': 'noShow']">
                        <div class="literature">
                            <p>(1)Qu naisi, Chu liangcheng, Guo yonggang, Perturbation of the Attached Water Mass Effect Offshore Platform Dynamic Response, China Ocean Engineering, Vol. 7, No. 4, 1993。</p>
                            <p>(2)Guo yonggang, Qu naisi, Perturbation Analysis of the Non-proportional Damping Effect Structure under the Arbitrary Load, EPMESC, Macao, 1995。 </p>
                            <p>(3)曲乃泗，初良成，郭永刚，动水非比例阻尼对平台结构影响的摄动分析，海洋通报，1994.12。</p>
                            <p>(4)郭永刚，曲乃泗，非比例阻尼对结构动力响应影响的摄动分析方法，地震工程与工程振动，1995年4期。</p>
                            <p>(5)郭永刚，董毓新，不同垫层材料对水轮机蜗壳结构的影响研究，大电机技术，1996年4期。 </p>
                            <p>(6)水工结构中载荷识别的时域法。</p>
                            <p>(7)掺入膨胀剂桩受力机理的试验研究。</p>
                            <p>(8)动接触问题在高拱坝抗震中的应用。 </p>
                            <p>(9)郭永刚，侯顺载，陈厚群等，高拱坝伸缩横缝的开合对拱座岩体稳定的影响研究，水利学报，2000年，第11期。 </p>
                            <p>(10)郭永刚，张祁汉，三峡水电站厂房结构自振特性研究，水力发电，2002.1。 </p>
                            <p>(11)郭永刚，周红卫等，大型渡槽结构减振隔振几个关键问题初探，现代地震工程进展，2002.10。 </p>
                            <p>(12)郭永刚，胡晓等，300米级高拱坝振动台模型试验研究，现代地震工程进展，2002.10。 </p>
                            <p>(13)郭永刚，涂劲，陈厚群，高拱坝伸缩横缝间布设阻尼器对坝体地震影响的研究，世界地震工程，2003.9。 </p>
                            <p>(14)涂劲，郭永刚，陈厚群，高拱坝抗震钢筋配置方案研究，水利水电技术，2003.7。 </p>
                            <p>(15)傅朝阳，郭永刚，李家峡水电站拱坝强震监测台阵的布设，水电自动化与大坝监测，2004.2。 </p>
                            <p>(16)郭永刚，涂劲，陈厚群，抗震钢筋对小湾高拱坝抗震性能影响研究，水利学报，2004.3。 </p>
                            <p>(17)郭永刚，赵晓飞等，考虑流—固耦合影响的挡水结构自振特性，世界地震工程，2004.9。 </p>
                            <p>(18)马飞，郭永刚，水小平，基于小波理论的振动信号的多尺度分析，噪声与振动控制，2004年12月，第6期。</p>
                        </div>
                        <el-pagination background layout="prev, pager, next" :total="50"></el-pagination>
                    </div>
                    <div :class="[activeIndex === 'science' ? 'simple': 'noShow']">
                        <div class="literature">
                            <p>(1)完成了“莲花水电站钢衬钢筋混凝土蜗壳结构三维非线性有限元计算分析”项目。</p>
                            <p>(2)完成了“三峡工程水电站厂房结构动力分析及优化”项目。</p>
                            <p>(3)完成了“三峡工程水电站压力钢管伸缩节问题的论证”项目。</p>
                            <p>(4)完成了“白山重力拱坝安全可靠性分析”项目。</p>
                            <p>(5)完成了“非比例阻尼问题及水电站结构动静力分析”。</p>
                            <p>(6)完成了原国电公司重点科技项目“小湾拱坝工程抗震关键技术深化研究”。</p>
                            <p>(7)完成了国家自然科学基金“大型渡槽结构减震隔振关键技术研究”。</p>
                            <p>(8)完成了原国家电力公司科技项目“混凝土高拱坝震害预警与决策系统研究”。</p>
                            <p>(9)完成了国家自然科学基金重点项目“西南地区复杂岩质高边坡变形与稳定性分析方法研究”中的子题“强震条件下边坡的动力变形与稳定性评价研究”的相关。</p>
                            <p>(10)完成了“长江三峡水利枢纽大坝和电站厂房二期二标段安全监测”分项“大坝强震监测”工作。</p>
                            <p>(11)完成了“金沙江下游梯级水电站水库地震监测系统一期工程”项目监理工作。</p>
                            <p>(12)完成了“二滩二副厂房泄洪振动原型观测分析”工作。</p>
                            <p>(13)完成了“小浪底进水塔及左岸山体振动原型观测与分析”工作。</p>
                            <p>(14)完成了“昆明市掌鸠河引水供水工程云龙水库诱发地震危险性预测研究”工作。</p>
                            <p>(15)完成了“西龙池抽水蓄能电站地下厂房中导洞开挖爆破围岩振动监测分析”工作。</p>
                            <p>(16)承担完成了“杨家台水库续建工程堆石坝振动测试与分析”工作。</p>
                            <p>(17)承担完成了九五攻关子子题项目“横缝对高拱坝抗震性能影响的数值分析研究”（编号96-221-03-02-02(3)。</p>
                            <p>(18)承担完成了国家防汛抗旱总指挥部办公室项目“密云水库、潘家口水库地震应急自动处置系统研究”工作。</p>
                        </div>
                        <el-pagination background layout="prev, pager, next" :total="50"></el-pagination>
                    </div>
                    <div :class="[activeIndex === 'software' ? 'simple': 'noShow']">
                        <div class="block">
                            地震<br />信息管理系统
                        </div>
                        <div class="block">
                            滑坡<br />信息管理系统
                        </div>
                        <div class="block">
                            泥石流
                        </div>
                        <div class="block"></div>
                    </div>
                    <div :class="[activeIndex === 'apparatus' ? 'simple': 'noShow']">
                        <div class="block">
                            地震<br />信息管理系统
                        </div>
                        <div class="block">
                            滑坡<br />信息管理系统
                        </div>
                        <div class="block">
                            泥石流
                        </div>
                        <div class="block"></div>
                    </div>
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