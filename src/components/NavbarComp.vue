<template>
  <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" :ellipsis="false" @select="handleSelect">
    <el-menu-item index="0">
      <h1>LOGO</h1>
    </el-menu-item>
    <el-menu-item>
      <el-input v-model="searchTerm" class="w-50 m-2" size="large" placeholder="Search .." :prefix-icon="Search" />
    </el-menu-item>
    <div class="flex-grow" />
    <el-menu-item index="1">
      <el-icon><House /></el-icon>Homepage</el-menu-item
    >
    <el-menu-item index="2"
      ><el-icon><User /></el-icon>Connections</el-menu-item
    >
    <el-menu-item index="3"
      ><el-icon><ChatSquare /></el-icon>Messages</el-menu-item
    >
    <el-menu-item index="4" style="border-right: 1px solid #e3e3e3"
      ><el-icon><BellFilled /></el-icon>Notification</el-menu-item
    >
    <el-menu-item index="5"
      ><el-icon><Box /></el-icon>Tools</el-menu-item
    >

    <el-menu-item>
      <el-avatar shape="square" fit="fill" src="https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg" />
      <span style="margin-left: 5px;"><b>Maruthi M B</b></span>
    </el-menu-item>
  </el-menu>
</template>

<script setup>
import { ref } from 'vue'
import { House, Search, BellFilled, User, ChatSquare, Box } from '@element-plus/icons-vue'

const activeIndex = ref('1')
const searchTerm = ref('')

const handleSelect = (key, keyPath) => {
  console.log(key, keyPath)
}
</script>

<style lang="scss" scoped>
.flex-grow {
  flex-grow: 1;
}
</style>
