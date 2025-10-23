<template>
  <div class="footer-container">
    <n-layout-footer class="custom-footer" bordered>
      <div style="padding: 12px 24px;">
        Driven by Bug and written by Fox
      </div>
    </n-layout-footer>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.footer-container {
  /* 居中定位 */
  position: fixed;
  bottom: 2%; /* 距离底部2% */
  left: 50%; /* 先定位到中间 */
  transform: translateX(-50%); /* 再通过偏移实现居中 */
  z-index: 1000; /* 确保在其他元素之上 */
}

.custom-footer {
  /* 添加一些样式使悬浮效果更明显 */
  border-radius: 15px; /* 圆角 */
  background-color: rgba(255, 255, 255, 0.7); /* 半透明背景 */
  backdrop-filter: blur(10px); /* 毛玻璃效果 */
  box-shadow: 0 -4px 20px rgba(0, 0, 0, 0.1); /* 阴影效果 */
  border: 1px solid rgba(255, 255, 255, 0.3); /* 边框 */
}
</style>