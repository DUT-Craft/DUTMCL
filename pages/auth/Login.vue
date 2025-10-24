<template>
  <div>
    <n-card>
      <n-anchor :show-rail="false" :bound="10">
        <n-anchor-link title="DUT猫娘社" @click="changeToDut"/>
        <n-anchor-link title="MUA联合" @click="changeToMUA"/>
        <n-anchor-link title="正版" @click="changeToGenuine"/>
        <n-anchor-link title="LittleSkin" @click="changeToLittleSkin"/>
        <n-anchor-link title="三方登录" @click="changeToTripartite"/>
        <n-anchor-link title="离线登录" @click="changeToOffline"/>
      </n-anchor>
    </n-card>
    <n-card>
      <component :is="LoginType"></component>
    </n-card>

  </div>
</template>

<script lang="ts" setup>
import DUT from "@/pages/LoginType/DUT.vue"
import MUA from "@/pages/LoginType/MUA.vue"
import Genuine from "@/pages/LoginType/Genuine.vue"
import LittleSkin from "@/pages/LoginType/LittleSkin.vue"
import Tripartite from "@/pages/LoginType/Tripartite.vue"
import Offline from "@/pages/LoginType/Offline.vue"
import {ref} from 'vue'


const LoginType = ref(DUT);

function changeToDut() {
  LoginType.value = DUT
}

function changeToMUA() {
  LoginType.value = MUA
}

function changeToGenuine() {
  LoginType.value = Genuine
}

function changeToLittleSkin() {
  LoginType.value = LittleSkin
}

function changeToTripartite() {
  LoginType.value = Tripartite
}

function changeToOffline() {
  LoginType.value = Offline
}
</script>

<style scoped>

</style>