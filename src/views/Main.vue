<template>
    <el-container class="main_container">
        <!-- 头部布局 -->
        <el-header>
            <!-- logo和项目名称 -->
            <div class="left_box">
                <img src="../assets/Img/chuyin.gif" alt="">
                <span>物资管理系统</span>
            </div>
            <!-- 用户登陆展示头像 -->
            <div class="right_box">
                <el-dropdown>
                    <img src="../assets/Img/chuyin.gif" alt="">
                    <!-- 下拉菜单 -->
                    <el-dropdown-menu slot="dropdown">
                        <el-dropdown-item icon="el-icon-house">系统首页</el-dropdown-item>
                        <el-dropdown-item icon="el-icon-ship">交流讨论</el-dropdown-item>
                        <el-dropdown-item icon="el-icon-swich-button">退出登陆</el-dropdown-item>
                    </el-dropdown-menu>
                </el-dropdown>

            </div>
        </el-header>

        <el-container>
            <!-- 侧边栏 -->
            <el-aside width="200px">
                <!-- 展开折叠 -->
                <div class="toggle_box">

                </div>
                <el-menu default-active="2" class="el-menu-vertical-demo"
                @open="handleOpen" @close="handleClose" :collapse="isCollapse"
                background-color="#66CCFF" text-color="#fff" active-text-color="#fff">
                    <el-submenu index="1">
                        <template slot="title">
                            <i class="el-icon-location"></i>
                            <span>用户管理</span>
                        </template>
                        <el-menu-item index="1-1">
                            <i class="el-icon-location"></i>
                            <span slot="title">管理</span>
                        </el-menu-item>
                    </el-submenu>

                    <el-submenu index="2">
                        <template slot="title">
                            <i class="el-icon-location"></i>
                            <span>用户管理</span>
                        </template>
                        <el-menu-item index="2-1">
                            <i class="el-icon-location"></i>
                            <span slot="title">管理</span>
                        </el-menu-item>
                    </el-submenu>
                </el-menu>
            </el-aside>

            <el-main>main</el-main>
        </el-container>
    </el-container>
</template>

<script>
export default {
    name: "Main",
    data(){
        return{
            isCollapse: true
        };
    }
}
</script>

<style scoped>
    /* 整个容器 */
    .main_container{
        height: 100%;
    }

    /* 头部布局 */
    .el-header{
        background-color: #39C5BB;
        /* background-color: rgb(255, 165, 0); */
        display: flex;
        justify-content: space-between;
        /* color:#39C5BB; */
        color: #fff;
        padding-left: 0;
        align-items: center;

    }
    .left_box, .right_box{
        display: flex;
        align-items: center;
    }
    .left_box > img{
        width: 55px;
        height: 55px;
        margin: 10px 0 10px 10px;
    }
    .left_box > span{
        margin-left: 15px;
    }
    .el-dropdown > img{
        width: 60px;
        height: 60px;
        border-radius: 50%;
        margin: 10px 0;
    }
    .right_box img{
        width: 55px;
        height: 55px;

    }

    /* 侧边栏 */
    .el-aside{
        background-color: #66CCFF;
        /* background-color: rgb(255, 226, 17); */
        /* color: rgb(255, 192, 203); */
        color: #fff;


    }

    /* 内容主体 */
    .el-main{
        background-color: #fff;
        color: rgb(255, 165, 0);
        text-align: center;
        line-height: 160px;
    }


    /* 下拉菜单样式 */
    .el-dropdown-link{
        cursor: pointer;
        color: #39C5BB;
    }
    /* .el-icon-arrow-down{
        font-size: 12px;
    }
    .demonstration{
        display: block;
        color: #444;
        font-size: 14px;
        margin-bottom: 20px;
    } */
</style>