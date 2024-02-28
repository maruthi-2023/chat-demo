<template>
  <el-row>
    <el-col :span="16">
      <div class="grid-content">
        <el-card class="box-card">
          <ChatWidget />
        </el-card>
      </div>
    </el-col>
    <el-col :span="8">
      <div class="grid-content">
        <el-card class="box-card">
          <template #header>
            <div class="card-header">
              <span><b>Advertising</b></span>
            </div>
            <div>
              <el-image style="width: 100%; height: 100%; padding: 2rem 0" src="https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg" fit="fill" />
            </div>
            <div style="text-align: center">
              <a href="#">Visit Website</a>
            </div>
          </template>
          <div class="display: flex">
            <a style="color: gray" href="#">Privacy Terms</a>
            <a style="color: gray; margin-inline: 1rem" href="#">Advertizing</a>
            <a style="color: gray" href="#">Cookies</a>
          </div>
          <template #footer>TalentWide @2024</template>
        </el-card>
      </div>
    </el-col>
  </el-row>
</template>

<script setup>
import ChatWidget from '../views/comps/ChatWidget.vue'
</script>

<style lang="scss">
.el-row {
  padding: 0px;
  margin: 0px;
  margin-inline: auto;
  background-color: #e3e3e3;
  min-height: 100vh;
}

.box-card {
  background-color: #fff;
  padding: 1rem;
  margin: 1rem;
  border-radius: 0.5rem;
}
</style>
