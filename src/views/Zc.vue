<template>
  <div>
    <Nav style="background-color:#5d80f5" />
    <div class="zuc">
      <div class="content">
        <!-- 步骤条 -->
        <el-steps :active="active" align-center>
          <el-step title="注册须知"></el-step>
          <el-step title="手机验证"></el-step>
          <el-step title="设置账号密码"></el-step>
          <el-step title="完成注册"></el-step>
        </el-steps>
      </div>
      <!-- 第一步协议 -->
      <div v-if="active===0">
        <div class="Xieyi">
          <div class="content-txt">
            <h2>“饿了么”开放平台在线服务协议</h2>
            <br />
            <p>协议版本： 2020年1月7日</p>
            <p>签署须知： 本服务协议（以下简称“本协议”）是上海拉扎斯信息科技有限公司（以下称甲方一）、拉扎斯网络科技（上海）有限公司（以下称甲方二，甲方一和甲方二合称“饿了么”）与服务商（以下或称为“您”）就您入驻开放平台有关的事宜所订立的有效合约。当您按照注册页面提示填写信息、阅读并同意本协议且完成全部注册程序后，即表示您已充分阅读、理解并接受本协议的全部内容，并与“饿了么”达成一致，成为“饿了么”开放平台的服务商。阅读本协议的过程中，如果您不同意本协议或其中任何条款约定，您应立即停止注册程序。本协议内容同时包括饿了么开放平台上现有及将来可能发布并采取合理途径通知的协议、业务规则、管理规范等内容。</p>
            <h3>一、定义</h3>
            <ol>
              <li>服务市场：指用户挑选您发布的应用及进行订阅或订购的自助服务市场和管理系统。</li>
              <li>开放平台：由“饿了么”所拥有并独立经营的 https://open.shop.ele.me 网站及相关页面。</li>
              <li>服务商：指您，按照开放平台流程经有效注册、申请后，通过开放平台进行应用开发或完善并提供咨询、操作等有偿服务的法人或其他组织。</li>
              <li>用户：指可通过服务市场订阅、达成交易意向等方式获取服务商服务或使用服务商所开发应用的“饿了么”平台商家。</li>
              <li>应用：指您基于开放平台所开发的软件或服务。本协议所称“应用”均指您发布并展示于服务市场的主应用，不包含其利用服务市场的相关服务能力、针对主应用的业务场景独立开发的、内置于主应用、可供用户单独订购的主应用的增值功能或服务（以下简称“内购应用”）。</li>
              <li>店铺和店铺ID（shopId）：用户在饿了么外卖平台上所开设的网络店铺，以及店铺的唯一标识数字。需要注意的是，用户和店铺是一对多的关系，即一个商户可以开设和管理多家店铺。</li>
              <li>Key： 应用的身份标识，全局唯一的一个字符串。</li>
              <li>Secret： 应用的私钥，一般配合应用的Key一起成对使用，用来验证应用的合法性。</li>
              <li>API（Application Programming Interface）：开放平台为第三方应用接入提供的编程接口，具体接口说明，参见API文档列表。</li>
              <li>授权： 您所开发的应用想要访问用户的店铺信息，则必须经过用户的同意，由应用发起的用户是否同意访问的操作称之为授权。</li>
              <li>推送： 开放平台向应用发送“新订单”、“运单状态变化”等消息，称之为向应用推送息。</li>
              <li>回调： 用户同意或拒绝应用的授权请求后，开放平台打开应用设置的回调URL并附加上商户同意或拒绝的操作信息，称为开放平台回调应用。</li>
              <li>聚石塔：指基于阿里巴巴数据分享战略、依托于云计算技术、联合电商行业开发者合作伙伴，帮助企业快速发展电子商务的开放的电商云工作平台。</li>
              <li>聚石塔内调用：指部署在聚石塔环境内的系统和应用发起的对饿了么开放平台API的使用行为，聚石塔环境包括聚石塔的云主机、应用运行引擎和托管主机等，以开发者发起调用的IP地址是否属于安全云环境认定的IP范围为准。</li>
              <li>聚石塔外调用：指由聚石塔环境外的系统和应用发起的对饿了么开放平台API的使用行为。</li>
            </ol>
            <h3>二、注册和更新</h3>
            <ol>
              <li>服务市场：指用户挑选您发布的应用及进行订阅或订购的自助服务市场和管理系统。</li>
              <li>开放平台：由“饿了么”所拥有并独立经营的 https://open.shop.ele.me 网站及相关页面。</li>
              <li>服务商：指您，按照开放平台流程经有效注册、申请后，通过开放平台进行应用开发或完善并提供咨询、操作等有偿服务的法人或其他组织。</li>
              <li>用户：指可通过服务市场订阅、达成交易意向等方式获取服务商服务或使用服务商所开发应用的“饿了么”平台商家。</li>
              <li>应用：指您基于开放平台所开发的软件或服务。本协议所称“应用”均指您发布并展示于服务市场的主应用，不包含其利用服务市场的相关服务能力、针对主应用的业务场景独立开发的、内置于主应用、可供用户单独订购的主应用的增值功能或服务（以下简称“内购应用”）。</li>
              <li>店铺和店铺ID（shopId）：用户在饿了么外卖平台上所开设的网络店铺，以及店铺的唯一标识数字。需要注意的是，用户和店铺是一对多的关系，即一个商户可以开设和管理多家店铺。</li>
              <li>Key： 应用的身份标识，全局唯一的一个字符串。</li>
              <li>Secret： 应用的私钥，一般配合应用的Key一起成对使用，用来验证应用的合法性。</li>
              <li>API（Application Programming Interface）：开放平台为第三方应用接入提供的编程接口，具体接口说明，参见API文档列表。</li>
              <li>授权： 您所开发的应用想要访问用户的店铺信息，则必须经过用户的同意，由应用发起的用户是否同意访问的操作称之为授权。</li>
              <li>推送： 开放平台向应用发送“新订单”、“运单状态变化”等消息，称之为向应用推送息。</li>
              <li>回调： 用户同意或拒绝应用的授权请求后，开放平台打开应用设置的回调URL并附加上商户同意或拒绝的操作信息，称为开放平台回调应用。</li>
              <li>聚石塔：指基于阿里巴巴数据分享战略、依托于云计算技术、联合电商行业开发者合作伙伴，帮助企业快速发展电子商务的开放的电商云工作平台。</li>
              <li>聚石塔内调用：指部署在聚石塔环境内的系统和应用发起的对饿了么开放平台API的使用行为，聚石塔环境包括聚石塔的云主机、应用运行引擎和托管主机等，以开发者发起调用的IP地址是否属于安全云环境认定的IP范围为准。</li>
              <li>聚石塔外调用：指由聚石塔环境外的系统和应用发起的对饿了么开放平台API的使用行为。</li>
            </ol>
          </div>

          <label>
            <input type="checkbox" class="checkbox" @click="checkbox" />我已同意《开放平台服务协议》
          </label>
        </div>
      </div>
      <!-- 第二步手机验证 -->
      <div v-if="active===1">
        <div class="phone">
          <el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="80px">
            <el-form-item label="手机号">
              <el-input v-model="ruleForm.phone">
                <template slot="append">获取验证码</template>
              </el-input>
            </el-form-item>
            <el-form-item label="验证码">
              <el-input v-model="ruleForm.pas"></el-input>
            </el-form-item>
          </el-form>
        </div>
      </div>
      <!-- 第三步 -->
      <div v-if="active===2"></div>
      <!-- 第四步 -->
      <div v-if="active===3"></div>
      <!-- 按钮 -->

      <div>
        <el-button
          type="primary"
          style="margin-top: 12px;"
          class="prev"
          @click="prev"
          v-if="active==1 || active==2 ||active==3 ||active ==4"
        >上一步</el-button>
        <el-button
          style="margin-top: 12px;"
          class="next"
          type="primary"
          @click="next"
          :disabled="disabled"
          v-if="active==0 || active==1 ||active==2 ||active ==3"
        >下一步</el-button>
        <el-button
          class="sub"
          type="primary"
          style="margin-top: 12px;"
          v-if="active==4"
          @click="submit"
        >提交</el-button>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  components: {
    Nav
  },
  data() {
    return {
      active: 0,
      disabled:true,
      
      ruleForm: {
        phone: "",
        pas: ""
      },
      rules: {
        phone: [{ required: true, message: "请输入手机号" }],
        pas: [{ required: true, message: "请输入验证码" }]
      }
    };
  },
  methods: {
    prev() {
      --this.active;
      if (this.active < 0) this.active = 0;
    },
    next(formName) {
      if (this.active++ > 3) this.active = 0;
      this.$refs[formName].validate(valid => {
        if (valid) {
          alert("submit!");
        } else {
          console.log("error submit!!");
          return false;
        }
      });
    },
    submit() {
      this.$message({
        message: "恭喜你，信息提交成功",
        type: "success"
      });
    },
    checkbox() {
      this.disabled=!this.disabled;
    }
  }
};
import "../assets/index.css";
import Nav from "../views/Nav";
</script>

<style>
</style>