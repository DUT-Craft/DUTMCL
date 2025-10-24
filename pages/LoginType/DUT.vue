<template>
  <div class="container">
      <div class="form">
        <n-button @click="toDut">欢迎使用DUT猫娘社登录，点击访问DUT猫窝</n-button>
        <n-space vertical>
          <div class="input-group">
            <label class="input-label">账号：</label>
            <n-input v-model:value="account" placeholder="请在这里输入账号喵" type="text"/>
          </div>
          <div class="input-group">
            <label class="input-label">密码：</label>
            <n-input v-model:value="password" placeholder="请在这里输入密码喵" show-password-on="mousedown" type="password"/>
          </div>
        </n-space>
        <n-button @click="login" type="primary" block>登录喵</n-button>
      </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const account = ref('')
const password = ref('')
const login = () => {
  console.log(account.value, password.value)
}

const toDut = () => {
  window.open('https://dut.cat')
}

</script>

<style scoped>
/* 页面容器样式 - 用于居中显示登录表单 */
.container {
  /* 使用 flex 布局实现水平垂直居中 */
  display: flex;
  justify-content: center;
  align-items: center;
  /* 占满整个视口 */
  width: 100vw;
  height: 100vh;
  /* 固定定位，确保居中效果 */
  position: fixed;
  top: 0;
  left: 0;
}


/* 表单样式 */
.form {
  padding: 20px;
}

/* 输入组样式 - 使标签和输入框在同一行 */
.input-group {
  /* 使用 flex 布局实现行内对齐 */
  display: flex;
  align-items: center;
  /* 设置底部间距 */
  margin-bottom: 20px;
}

/* 输入标签样式 */
.input-label {
  /* 固定宽度确保对齐一致性 */
  width: 60px;
  /* 设置右边距 */
  margin-right: 10px;
  /* 文本右对齐 */
  text-align: right;
}

/* 登录按钮样式 */
:deep(.n-button) {
  margin-top: 10px;
  background: thistle;
}
</style>