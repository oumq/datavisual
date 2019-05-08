<template>
  <div>
    <div class="login-logo">
      <img src="@/assets/login/bear.jpg" style="width:200px;height:200px">
    </div>
    <el-form
      ref="loginForm"
      :model="account"
      :rules="rules"
      label-position="left"
      label-width="0px"
      class="login-container"
    >
      <h3>系统登录</h3>
      <el-form-item
        prop="username"
        class="login-item"
      >
        <el-input
          type="text"
          v-model="account.username"
          auto-complete="off"
          placeholder="账号"
        ></el-input>
      </el-form-item>
      <el-form-item
        prop="pwd"
        class="login-item"
      >
        <el-input
          type="password"
          v-model="account.pwd"
          auto-complete="off"
          placeholder="密码"
        ></el-input>
      </el-form-item>
      <el-form-item class="login-item">
        <el-button
          type="primary"
          style="width:100%;"
        >登录</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>

export default {
  name: 'login',
  data () {
    return {
      account: {
        username: '',
        pwd: ''
      },
      rules: {
        username: [
          {
            required: true,
            message: '请输入账号',
            trigger: 'blur'
          }
        ],
        pwd: [
          {
            required: true,
            message: '请输入密码',
            trigger: 'blur'
          }
        ]
      }
    }
  }
}
</script>

<style scoped>
.login-logo {
  margin: 60px auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
.login-container {
  width: 350px;
  margin-left: 35%;
  /*box-shadow: 0 0px 8px 0 rgba(0, 0, 0, 0.06), 0 1px 0px 0 rgba(0, 0, 0, 0.02);*/
  -webkit-border-radius: 5px;
  border-radius: 5px;
  -moz-border-radius: 5px;
  background-clip: padding-box;
  margin: 0 auto;
  padding: 35px 35px 15px 35px;
  background: #fff;
  border: 1px solid #eaeaea;
  box-shadow: 0 0 25px #cac6c6;
}
.login-item {
  margin-top: 35px;
}
</style>
