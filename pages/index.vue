<template>
  <!-- 页面容器 -->
  <div class="page-container">
    <!-- 全屏显示的图片 -->
    <n-image
      class="full-screen-image"
      src="/back.png"
      preview-disabled
      object-fit="fill"
    />
    <LayoutFooter />
  </div>
</template>

<script setup lang="ts">
// 导入 naive-ui 图片组件
import { NImage } from 'naive-ui'
</script>

<style scoped>
/* 页面容器样式 */
.page-container {
  /* 占满整个视图 */
  width: 100vw;
  height: 100vh;
  
  /* 使用 flex 布局 */
  display: flex;
  flex-direction: column;
  
  /* 避免滚动条影响视图尺寸 */
  box-sizing: border-box;
  
  /* 确保内容不会溢出 */
  overflow: hidden;
}

/* 全屏图片样式 */
.full-screen-image {
  /* 自动填充整个容器 */
  width: 100%;
  height: 100%;
  
  /* 强制拉伸图片以完全填充容器 */
  object-fit: fill;
  
  /* 添加过渡效果使尺寸变化更平滑 */
  transition: all 0.3s ease;
}
</style>