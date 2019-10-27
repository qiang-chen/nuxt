<template>
  <div class="main">
    <el-container style="display: flex;flex-direction: column;width: 100%;height: 100%;">
      <el-header style="height:64px;">
        <div class="main-header">
          <img src="../static/images/timg.jpg">
        </div>
      </el-header>
      <el-main style="flex: 1;width: 100%;height: 100%;">
        <el-row class="tac" style="width: 100%;height: 100%;display: flex;">
          <el-col :span="4" style="height: 100%;min-width: 204px;">
            <el-menu
              class="el-menu-vertical-demo"
              background-color="#232A41"
              text-color="rgba(255, 255, 255, 0.65)"
              active-text-color="#ffd04b">
              <el-submenu index="1">
                <template slot="title">
                  <i class="el-icon-location"></i>
                  <span>试题管理</span>
                </template>
                <el-menu-item-group>
                  <el-menu-item index="1-1" @click="addTestQuestions">添加试题</el-menu-item>
                  <el-menu-item index="1-2">试题分类</el-menu-item>
                  <el-menu-item index="1-3">查看试题</el-menu-item>
                </el-menu-item-group>
              </el-submenu>
              <el-submenu index="2">
                <template slot="title">
                  <i class="el-icon-menu"></i>
                  <span slot="title">用户管理</span>
                </template>
                <el-menu-item-group>
                  <el-menu-item index="2-1">添加用户</el-menu-item>
                  <el-menu-item index="2-2">用户展示</el-menu-item>
                </el-menu-item-group>
              </el-submenu>
              <el-submenu index="3">
                <template slot="title">
                  <i class="el-icon-document"></i>
                  <span slot="title">考试管理</span>
                </template>
                <el-menu-item-group>
                  <el-menu-item index="3-1">添加考试</el-menu-item>
                  <el-menu-item index="3-2">试卷列表</el-menu-item>
                </el-menu-item-group>
              </el-submenu>
              <el-submenu index="4">
                <template slot="title">
                  <i class="el-icon-setting"></i>
                  <span slot="title">班级管理</span>
                </template>
                <el-menu-item-group>
                  <el-menu-item index="4-1">班级管理</el-menu-item>
                  <el-menu-item index="4-2">教室管理</el-menu-item>
                  <el-menu-item index="4-2">学生管理</el-menu-item>
                </el-menu-item-group>
              </el-submenu>
              <el-submenu index="5">
                <template slot="title">
                  <i class="el-icon-bell"></i>
                  <span slot="title">阅卷管理</span>
                </template>
                <el-menu-item-group>
                  <el-menu-item index="5-1">待批班级</el-menu-item>
                </el-menu-item-group>
              </el-submenu>
            </el-menu>
          </el-col>
          <el-col :span="20" style="flex: 1;height: 100%;background-color: #f0f2f5;padding: 0 24px;">
            <nuxt-child/>
          </el-col>
        </el-row>
      </el-main>
    </el-container>
  </div>
</template>

<script>
  export default {
    name: 'HomeIndex',
    methods:{
      addTestQuestions(){
        this.$router.push('/home/addTestQuestions');
      }
    }
  }
</script>

<style scoped lang="scss">
  @import "../assets/scss/common";

  .main {
    @include whall;

    .main-header {
      @include wall;
      height: 64px;
      background: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, .19) !important;
      position: fixed !important;
      left: 0;
      top: 0 !important;
      z-index: 100 !important;
      padding: 0 50px;
      display: flex;
      align-items: center;
      justify-content: space-between;

      img {
        height: 46%;
      }
    }

    .el-menu-vertical-demo {
      width: 100%;
      height: 100%;

      /deep/ .el-submenu__icon-arrow {
        margin-top: -6px;
      }
    }
  }
</style>
