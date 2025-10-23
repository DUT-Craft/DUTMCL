<template>
  <div class="layout-container">
    <TopNavigationBar />
    <slot/>
  </div>
</template>

<script setup lang="ts">



</script>

<style scoped>
.layout-container {
  /* 占满整个视图 */
  width: 100vw;
  height: 100vh;
  
  /* 使用 flex 布局 */
  display: flex;
  flex-direction: column;
  
  /* 避免滚动条影响视图尺寸 */
  box-sizing: border-box;
}
</style>