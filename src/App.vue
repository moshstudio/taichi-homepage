<script setup lang="ts">
import TaiChi from './components/TaiChi.vue'
const toGithub = () => {
  window.open('https://github.com/moshstudio/TAICHI-flet')
}
const toDownload = () => {
  window.location.href = 'https://taichi.s3.bitiful.net/taichi.exe?no-wait=on'
}
</script>

<template>
  <div class="wrapper">
    <TaiChi />
    <div class="title">太极神器</div>
    <div class="buttons">
      <button @click="toGithub">查看介绍</button>
      <button @click="toDownload">立即下载</button>
    </div>
  </div>
</template>

<style>
/* 全局样式 - 确保 #app 占满全屏 */
html,
body {
  margin: 0;
  padding: 0;
  height: 100%;
  overflow: hidden; /* 防止滚动条出现 */
}

#app {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

#app::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image:
    linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)),
    /* 深色叠加层 */ url('./assets/taichi-bg.jpg');
  background-size: cover;
  background-position: center;
  filter: blur(8px);
  z-index: -1;
  transform: scale(1.1);
}
</style>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  position: relative; /* 确保内容在模糊背景之上 */
}
.title {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 20px;
  color: floralwhite;
}

.buttons {
  display: flex;
  gap: 12px;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
  margin-bottom: 40px;
}

button {
  padding: 0.5rem 1rem;
  border-radius: 0.5rem;
  border: 1px solid #ccc;
  background-color: #fff;
  cursor: pointer;
  transition: all 0.3s ease;
  user-select: none;
}

button:hover {
  background-color: #f0f0f0;
  transform: translateY(-2px);
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}
</style>
