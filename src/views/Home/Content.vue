<template>
  <div id="content">
    <h1 class="content-h1">资源优势和接入流程</h1>
    <div class="content-item">
      <div class="content-span1" :class="{cur:tab===1} " @click="tab=1">
        <!-- v-show="tab===1" -->
        <h3>平台服务商</h3>
        <span>提供经营管理增值服务</span>
      </div>
      <div class="content-span1" :class="{cur:tab===2} " @click="tab=2">
        <h3>企业服务商</h3>
        <span>提供订单商品基础服务</span>
      </div>
    </div>
    <div class="content-item1">
      <span>资源优势</span>
      <span>•</span>
      <span>接入流程</span>
    </div>
    <!-- 图标 -->
    <div class="content-item3">
      <div class="content-item-card" v-show="tab===1">
        <div class="content-item3-card1">
          <img src="../../assets/base8.png" alt />
          <h3>服务市场</h3>
          <p>打造专业服务市场，与商家端后台无缝对接，全平台分发您的应用</p>
        </div>
        <div class="content-item3-card1">
          <img src="../../assets/base10.png" alt />
          <h3>海量活跃商家</h3>
          <p>共享饿了么百万活跃商家资源，在线订购您的应用服务</p>
        </div>
        <div class="content-item3-card1">
          <img src="../../assets/base9.png" alt />
          <h3>丰富的 IT 工具</h3>
          <p>提供丰富的 API 接口，涵盖饿了么商家大量的核心功能，为合作伙伴提供多元服务</p>
        </div>
      </div>

      <div class="content-item-card" v-show="tab===2">
        <div class="content-item3-card1">
          <img src="../../assets/base8.png" alt />
          <h3>丰富的 IT 工具</h3>
          <p>提供测试工具、API 调试工具、服务监控、日志分析统计等丰富的解决方案</p>
        </div>
        <div class="content-item3-card1">
          <img src="../../assets/base10.png" alt />
          <h3>沙箱环境</h3>
          <p>数据独立，支撑开放业务功能测试需求</p>
        </div>
        <div class="content-item3-card1">
          <img src="../../assets/base9.png" alt />
          <h3>丰富的 API 接口</h3>
          <p>提供丰富的 API 接口，涵盖饿了么商家大量的核心功能，为合作伙伴提供多元服务</p>
        </div>
      </div>

      <div class="content-item4">
        <el-button class="shichang">入住服务市场</el-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tab: 1
    };
  }
};
</script>

<style>
</style>