<template>
  <div id="nav">
    <el-menu
      :default-active="activeIndex2"
      class="el-menu-demo"
      mode="horizontal"
      @select="handleSelect"
      text-color="#fff"
      active-text-color="#fff"
      background-color="transparent"
    >
      <a href class="logo">
        <img src="../assets/logo.png" alt />
        <span class="iconfont icon-dian">商家开放平台</span>
      </a>
      <el-menu-item index="1">
        <router-link to="/home">首页</router-link>
      </el-menu-item>
      <el-menu-item index="2">
        <router-link to="/about">文档中心</router-link>
      </el-menu-item>
      <el-menu-item index="3">管理中心</el-menu-item>
      <el-menu-item index="4">帮助中心</el-menu-item>
      <el-menu-item index="5">
        <el-input placeholder="搜索"></el-input>
        <span class="iconfont icon-shuxian1"></span>
      </el-menu-item>
      <el-menu-item index="6">
        <el-button type="text" @click="dialogVisible = true" style="color:white">登录</el-button>
        <el-dialog title="开发者账号登录" :visible.sync="dialogVisible" width="25%">
          <p class="text">一个应用可以授权多个商家</p>
          <el-input placeholder="开发者账号"></el-input>
          <br />
          <el-input placeholder="密码"></el-input>
          <div class="wj">
            <span>忘记密码</span>
            <span>手机验证码登录</span>
          </div>
          <div>
            <div class="dialog-footer">
              <el-button type="primary" @click="dialogVisible = false" class="qx">确 定</el-button>
              <el-button class="qx">
                <router-link to="/zc">注册</router-link>
              </el-button>
            </div>
            <div class="dialog-footer-text">
              <div>
                <span>商家账号登录</span>
                <br />
                <span id="span2">直接接入当前商家，无需授权</span>
              </div>
              <div>
                <span class="iconfont icon-you"></span>
              </div>
            </div>
          </div>
        </el-dialog>
      </el-menu-item>
      <el-menu-item index="7">
        <router-link to="/zc">
          <el-button class="zcbtn">注册</el-button>
        </router-link>
      </el-menu-item>
    </el-menu>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeIndex2: "1",
      dialogVisible: false
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
import "../assets/index.css";
</script>

<style>
/* @import "@/styles/main"; */
.active {
  color: #E6A23C;
}
</style>