<template>
  <!-- 页面容器 -->
  <div class="page-container">
    <!-- 全屏显示的背景图 -->
    <div 
      class="background-image"
      :style="{ backgroundImage: 'url(' + backgroundImage + ')' }"
    ></div>

    <n-card class="positioned-card" title="点击切换皮肤站">
      <n-button class="custom-button" @click="changeSkin">
        {{ skinType }}
      </n-button>
    </n-card>

    <LayoutFooter />

  </div>

</template>

<script setup lang="ts">
import { useMessage } from 'naive-ui'
// 导入背景图
const backgroundImage = '/back.png'
const message = useMessage()

const skinType = ref("猫娘社")

function changeSkin() {
  // 获取当前皮肤类型
  const currentSkin = skinType.value

  // 根据皮肤类型切换背景图
  switch (currentSkin) {
    case '猫娘社':
      message.info('喵！切换到MUA联合')
      skinType.value = 'MUA联合'
      break
    case 'MUA联合':
      message.info('喵！切换到正版')
      skinType.value = '正版'
      break
    case '正版':
      message.info('喵！切换到猫娘社')
      skinType.value = '猫娘社'
      break
  }
}
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
  
  /* 设置相对定位，以便子元素可以绝对定位 */
  position: relative;
}

/* 背景图片样式 */
.background-image {
  /* 完全覆盖容器 */
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  
  /* 背景图相关属性 */
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  
  /* 将背景图置于最底层 */
  z-index: -1;
  
  /* 添加模糊效果增强文字可读性 */
  filter: blur(2px) brightness(0.8);
}

/* 定位卡片样式 */
.positioned-card {
  /* 设置绝对定位 */
  position: absolute;
  
  /* 根据要求设置边距 */
  top: 20%;
  left: 5%;
  bottom: 70%;
  right: 80%;
  
  /* 确保卡片内容可见 */
  z-index: 1;
  
  /* 半透明背景 */
  background-color: rgba(255, 255, 255, 0.8);
  
  /* 毛玻璃效果 */
  backdrop-filter: blur(10px);
  
  /* 圆角 */
  border-radius: 15px;
  
  /* 阴影效果 */
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
  
  /* 边框 */
  border: 1px solid rgba(255, 255, 255, 0.3);
  
  /* 动画效果 */
  transition: all 0.3s ease;
}

/* 卡片悬停效果 */
.positioned-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.3);
}

/* 自定义按钮样式 */
.custom-button {
  /* 按钮颜色 */
  background: linear-gradient(45deg, #ff6b6b, #ffa5a5);
  border: none;
  color: white;
  
  /* 圆角 */
  border-radius: 20px;
  
  /* 内边距 */
  padding: 8px 20px;
  
  /* 字体 */
  font-weight: bold;
  
  /* 阴影 */
  box-shadow: 0 4px 15px rgba(255, 107, 107, 0.4);
  
  /* 过渡效果 */
  transition: all 0.3s ease;
}

/* 按钮悬停效果 */
.custom-button:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 20px rgba(255, 107, 107, 0.6);
}

/* 卡片描述文字样式 */
.card-description {
  font-size: 12px;
  color: #666;
  margin-top: 10px;
  text-align: center;
}
</style>