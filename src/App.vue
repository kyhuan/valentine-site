<script setup>
import { ref, onMounted } from 'vue'
import { StarFilled } from '@element-plus/icons-vue'
import gsap from 'gsap'
</script>

<template>
  <div class="valentine-container">
    <div class="message" ref="messageRef">
      <h1>祝</h1>
      <h1 class="name">张小宇</h1>
      <h1>情人节快乐</h1>
      <div class="hearts">
        <el-icon class="heart" v-for="n in 5" :key="n"><StarFilled /></el-icon>
      </div>
    </div>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Ma+Shan+Zheng&display=swap');

.valentine-container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #ff69b4, #ff1493);
  font-family: 'Ma Shan Zheng', cursive;
}

.message {
  text-align: center;
  color: white;
  padding: 2rem;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border-radius: 20px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
}

.message h1 {
  font-size: 4rem;
  margin: 0.5rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
}

.name {
  color: #ffd700;
  font-size: 5rem !important;
}

.hearts {
  margin-top: 2rem;
}

.heart {
  font-size: 2rem;
  color: #ffd700;
  margin: 0 0.5rem;
  animation: pulse 1.5s infinite;
}

@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.2); }
  100% { transform: scale(1); }
}
</style>
