<template>
  <!-- 顶部导航栏容器 -->
  <div class="navigation-container">
    <!-- 使用 naive-ui 的卡片组件创建带有圆角和透明效果的容器 -->
    <n-card class="custom-container" content-style="padding: 0;">
      <!-- 导航内容区域 -->
      <div class="nav-content">
        <!-- 首页导航按钮 -->
        <n-button class="nav-button" quaternary>
          <n-icon size="24">
            <AiFillHome/>
          </n-icon>
          <span class="button-text">首页</span>
        </n-button>
        
        <!-- 在线服务器导航按钮 -->
        <n-button class="nav-button" quaternary>
          <n-icon size="24">
            <AiFillHdd/>
          </n-icon>
          <span class="button-text">在线服务器</span>
        </n-button>
        
        <!-- 设置导航按钮 -->
        <n-button class="nav-button" quaternary>
          <n-icon size="24">
            <AiFillSetting/>
          </n-icon>
          <span class="button-text">设置</span>
        </n-button>
        
        <!-- 更多功能导航按钮 -->
        <n-button class="nav-button" quaternary>
          <n-icon size="24">
            <AiFillAppstore/>
          </n-icon>
          <span class="button-text">更多</span>
        </n-button>
      </div>
    </n-card>
  </div>
</template>

<script lang="ts" setup>
// 导入 naive-ui 图标组件
import {AiFillHome , AiFillSetting,AiFillHdd ,AiFillAppstore } from 'vue-icons-plus/ai'
</script>

<style scoped>
/* 导航栏容器样式 */
.navigation-container {
  /* 宽度占视图的90%，左右各留5%的边距 */
  width: 94%;
  /* 设置外边距：上边距5%，水平居中 */
  margin: 2% auto 0;
  /* 固定定位，使导航栏悬浮在页面顶部 */
  position: fixed;
  /* 距离顶部0，左右各5% */
  top: 0;
  left: 5%;
  right: 5%;
  /* 设置层级，确保导航栏在其他元素之上 */
  z-index: 1000;
}

/* 自定义容器样式 */
.custom-container {
  /* 宽度100%填充父容器 */
  width: 100%;
  /* 固定高度60px */
  height: 60px;

  /* 设置圆角，实现四角椭圆效果 */
  border-radius: 20px;

  /* 半透明背景色，实现40%透明度效果 */
  background-color: rgba(255, 255, 255, 0.7);
  /* 背景模糊效果，实现毛玻璃效果 */
  backdrop-filter: blur(10px);

  /* 边框线，增强视觉效果 */
  border: 1px solid rgba(255, 255, 255, 0.3);

  /* 阴影效果，增强悬浮感 */
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.15);
  
  /* 向下轻微偏移，增强悬浮感 */
  transform: translateY(5px);
}

/* 导航内容区域样式 */
.nav-content {
  /* 使用flex布局 */
  display: flex;
  /* 水平均匀分布子元素 */
  justify-content: space-around;
  /* 垂直居中 */
  align-items: center;
  /* 高度填充父容器 */
  height: 100%;
  /* 左右内边距 */
  padding: 0 10px;
}

/* 导航按钮样式 */
.nav-button {
  /* 使用flex布局，垂直排列图标和文字 */
  display: flex;
  flex-direction: column;
  /* 水平和垂直居中 */
  align-items: center;
  justify-content: center;
  /* 高度填充父容器 */
  height: 100%;
  /* 设置圆角 */
  border-radius: 15px !important;
  /* 添加过渡动画效果 */
  transition: all 0.3s ease;
  /* 设置文字颜色 */
  color: #333;
}

/* 导航按钮悬停效果 */
.nav-button:hover {
  /* 悬停时的背景色：粉红色且透明度30% */
  background-color: rgba(255, 192, 203, 0.7);
  /* 向上轻微移动，增强交互感 */
  transform: translateY(-2px);
}

/* 按钮文字样式 */
.button-text {
  /* 字体大小 */
  font-size: 12px;
  /* 上边距 */
  margin-top: 2px;
  /* 字体粗细 */
  font-weight: 500;
}

/* 响应式设计 - 针对小屏幕设备 */
@media (max-width: 768px) {
  /* 小屏幕下的按钮文字样式 */
  .button-text {
    font-size: 10px;
  }
  
  /* 小屏幕下的容器高度调整 */
  .custom-container {
    height: 50px;
  }
}
</style>