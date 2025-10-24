<template>
  <n-config-provider>
    <n-message-provider>
      <nuxt-layout>
        <nuxt-page style="min-height: calc(100dvh - 61px)"/>
      </nuxt-layout>
    </n-message-provider>
  </n-config-provider>
</template>

<script lang="ts" setup>
// 引入 Naive UI 组件库的配置提供者组件，用于全局配置 Naive UI 组件
import {NConfigProvider, NMessageProvider} from 'naive-ui';
// 全局样式导入
</script>