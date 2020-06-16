# el-app01

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

背景色 透明
```
background-color="transparent"
```
导航栏设置绝对定位
```
#nav {
    position: absolute;
    z-index: 9999999;
    width: 100%;
    top: 0;
}
```

其他组件引入导航组件，并设置背景色
```
 <Nav style="background-color:#5d80f5" />
 import Nav from "../views/Nav";
 components: {
    Nav
  },
```


el步骤条组件
```
 <el-steps :active="active" align-center>
          <el-step title="注册须知"></el-step>
          <el-step title="手机验证"></el-step>
          <el-step title="设置账号密码"></el-step>
          <el-step title="完成注册"></el-step>
 </el-steps>
 <div v-if="active===1">111</div>
 <div v-if="active===2">222</div>      
 <div v-if="active===3">333</div>
 <div v-if="active===4">444</div>
 //按钮
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
  data() {
    return {
      active: 0,
      disabled:true,
    };
    }
```
按钮方法
```
  methods:{
      prev() {
      --this.active;
      if (this.active < 0) this.active = 0;
    },
    next() {
      if (this.active++ > 3) this.active = 0;
    },
    submit() {
      this.$message({
        message: "恭喜你，信息提交成功",
        type: "success"
      });
    },
```
点击checkbox 解除按钮禁用
```
 <label>
      <input type="checkbox" class="checkbox" @click="checkbox" />我已同意《开放平台服务协议》
 </label>
 
 data(){
   disabled:true,//默认按钮不可用
 }
 //取反
 checkbox() {
      this.disabled=!this.disabled;
    }
```
