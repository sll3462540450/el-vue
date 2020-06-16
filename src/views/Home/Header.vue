<template>
  <!-- 走马灯 -->
  <div class="header">
    <div class="header-list">
      <el-carousel indicator-position="outside" height="540px">
        <el-carousel-item v-for="item in banners" :key="item.title">
          <h1>{{item.title}}</h1>
          <p>{{item.text}}</p>
          <el-button round class="btn">立即免费加入</el-button>
        </el-carousel-item>
      </el-carousel>
      <div class="home-new">
        <div>
          <span class="home-new-txt">new</span>
          <span class="home-new-txt1">关于服务市场转账手续费变更公告</span>
        </div>
        <div>
          <span class="home-new-txt">new</span>
          <span class="home-new-txt1">【接口变更】订单接口变更</span>
        </div>
        <div>
          <span class="home-new-txt1">全部公告 ></span>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Home",
  data() {
    return {
      banners: [
        {
          title: "饿了么开放平台，连接千万商家",
          text: "与 3,000+ 位开发者一起，共建 O2O 行业良性生态"
        },
        {
          title: "服务市场火热招募中",
          text: "优秀服务商集合地，点金共赢就等你来"
        }
      ]
    };
  }
};
import "../../assets/index.css";
</script>
<style>
</style>
