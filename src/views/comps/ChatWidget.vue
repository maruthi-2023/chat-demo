<template>
  <div class="chat">
    <div class="chat__left">
      <!-- message_header :: start -->
      <div style="display: flex; justify-content: space-between; padding: 1rem 0.5rem; border-bottom: 1px solid #e3e3e3">
        <div style="padding: 0.5rem"><b>Messages</b></div>
        <div>
          <div style="display: flex; justify-content: space-around">
            <div style="padding: 0.5rem">
              <el-icon><Plus /></el-icon>
            </div>
            <div style="padding: 0.5rem">
              <el-icon><More /></el-icon>
            </div>
          </div>
          <div></div>
        </div>
      </div>
      <!-- message_header :: end -->

      <!-- messageBody :: start -->
      <div style="display: flex; justify-content: space-between; align-items: center; padding: 0.5rem">
        <div style="padding: 0.5rem">
          <el-icon><Plus /></el-icon>
        </div>
        <div style="padding: 0.5rem">
          <el-input v-model="searchTerm" class="w-50 m-2" size="large" placeholder="Search .." :prefix-icon="Search" />
        </div>
        <div style="padding: 0.5rem">
          <el-icon><Filter /></el-icon>
        </div>
      </div>
      <!-- messageBody :: end -->

      <!-- messageFooter :: start -->
      <div v-for="item in 8" :key="item">
        <div style="display: flex; align-items: start; justify-content: space-between; border-bottom: 1px solid #e3e3e3; padding: 10px 2px">
          <div style="display: flex; align-items: center">
            <div style="margin-inline: 0.5rem">
              <el-avatar shape="square" :size="50" fit="fill" src="https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg" />
            </div>
            <div>
              <div>Naveen Kumar</div>
              <div>
                <small>Hi How are you ?</small>
              </div>
            </div>
          </div>
          <div>
            <small style="color: greyl; padding-right: 0.5rem">06 Jan</small>
          </div>
        </div>
      </div>
      <!-- messageFooter :: end -->
    </div>
    <div class="chat__right">
      <!-- containerHead :: start -->
      <div style="display: flex; justify-content: space-between; padding: 0.5rem">
        <div style="padding: 0.5rem">
          <div><h4>George Paul</h4></div>

          <div style="display: flex; align-items: center">
            <el-icon><Platform /></el-icon>
            <div style="margin-left: 0.5rem"><p>Online</p></div>
          </div>
        </div>
        <div>
          <div style="display: flex; justify-content: space-around">
            <div style="padding: 0.5rem">
              <el-icon><More /></el-icon>
            </div>
          </div>
          <div></div>
        </div>
      </div>
      <!-- containerHead :: end -->

      <!-- containerBody :: start -->
      <div style="min-height: 600px; background-color: #e3e3e3; padding: 0.5rem; margin: 0.5rem; border-radius: 0.8rem">
        <div style="display: flex; padding: 0.5rem 0rem; text-overflow: scroll; justify-content: start">
          <div style="margin-right: 0.5rem">
            <el-avatar shape="square" size="100" src="https://cube.elemecdn.com/9/c2/f0ee8a3c7c9638a54940382568c9dpng.png" />
          </div>
          <div style="border: 1px solid darkgray; padding: 1rem; border-radius: 0.5rem">Hi there how are you ?</div>
        </div>
        <div style="display: flex; padding: 0.5rem 0rem; text-overflow: scroll; justify-content: end">
          <div style="margin-right: 0.5rem">
            <el-avatar shape="square" size="100" src="https://cube.elemecdn.com/9/c2/f0ee8a3c7c9638a54940382568c9dpng.png" />
          </div>
          <div style="border: 1px solid darkgray; padding: 1rem; border-radius: 0.5rem">I am fine thanks, how are you ?</div>
        </div>
        <div style="display: flex; padding: 0.5rem 0rem; text-overflow: scroll; justify-content: end">
          <div style="margin-right: 0.5rem">
            <el-avatar shape="square" size="100" src="https://cube.elemecdn.com/9/c2/f0ee8a3c7c9638a54940382568c9dpng.png" />
          </div>
          <div style="border: 1px solid darkgray; padding: 1rem; border-radius: 0.5rem">How is your project going on ?</div>
        </div>
        <div style="display: flex; padding: 0.5rem 0rem; text-overflow: scroll; justify-content: end">
          <div style="margin-right: 0.5rem">
            <el-avatar shape="square" size="100" src="https://cube.elemecdn.com/9/c2/f0ee8a3c7c9638a54940382568c9dpng.png" />
          </div>
          <div style="border: 1px solid darkgray; padding: 1rem; border-radius: 0.5rem">I am fine thanks, how are you ?</div>
        </div>
        <div style="display: flex; padding: 0.5rem 0rem; text-overflow: scroll; justify-content: end">
          <div style="margin-right: 0.5rem">
            <el-avatar shape="square" size="100" src="https://cube.elemecdn.com/9/c2/f0ee8a3c7c9638a54940382568c9dpng.png" />
          </div>
          <div style="border: 1px solid darkgray; padding: 1rem; border-radius: 0.5rem">I am fine thanks, how are you ?</div>
        </div>
      </div>
      <!-- containerBody :: start -->

      <!-- containerFooter :: start -->
      <div>
        <el-card shadow="never" style="margin: 1rem 0.5rem">
          <div style="display: flex; justify-content: space-between; align-items: center">
            <div>
              <el-icon><Plus /></el-icon>
            </div>
            <div style="flex: 1; padding: 5px 10px">
              <el-input v-model="input1" class="w-50 m-2" placeholder="Message.." :suffix-icon="CopyDocument" />
            </div>
            <div>
              <el-icon><Microphone /></el-icon>
            </div>
          </div>
        </el-card>
      </div>
      <!-- containerFooter :: start -->
    </div>
  </div>
</template>

<script setup>
import { Plus, More, Platform, Filter, Search, Microphone, CopyDocument } from '@element-plus/icons-vue'
import { ref } from 'vue'
const input1 = ref('')
</script>

<style lang="scss" scoped>
.chat {
  display: flex;
  justify-content: center;
  width: 100%;
  &__left {
    width: 30%;
  }
  &__right {
    width: 70%;
  }
}
</style>
