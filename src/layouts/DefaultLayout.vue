<template>
  <div class="common-layout">
    <el-container>
      <!-- navbar :: start -->
      <el-header>
        <NavbarComp />
      </el-header>
      <!-- navbar :: end -->

      <!-- container :: start -->
      <el-main>
        <RouterView />
      </el-main>
      <!-- container :: end -->
    </el-container>
  </div>
</template>

<script setup>
import NavbarComp from '@/components/NavbarComp.vue'
</script>
