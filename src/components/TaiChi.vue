<template>
  <div class="taiji">
    <div class="tj white"></div>
    <div class="tj black"></div>
    <div class="round r-w">
      <div class="small s-b"></div>
    </div>
    <div class="round r-b">
      <div class="small s-w"></div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.taiji {
  background-color: gray;
  margin: 100px auto;
  position: relative;
  width: 240px;
  height: 240px;
  border-radius: 50%;

  animation: spin 100s linear infinite;
  user-select: none;
}
.tj {
  width: 50%;
  height: 100%;
  position: absolute;
  top: 0;
}
.white {
  background-color: white;
  left: 0;
  border-radius: 100% 0 0 100%/50% 0 0 50%;
}
.black {
  background-color: black;
  right: 0;
  border-radius: 0 100% 100% 0/0 50% 50% 0;
}
.round {
  width: 50%;
  height: 50%;
  border-radius: 50%;
  position: absolute;
}
.r-w {
  background-color: white;
  top: 0;
  left: 25%;
}
.r-b {
  background-color: black;
  bottom: 0;
  right: 25%;
}
.small {
  width: 25%;
  height: 25%;
  border-radius: 50%;
  position: absolute;
  left: 37.5%;
}
.s-b {
  background-color: black;
  top: 37.5%;
}
.s-w {
  background-color: white;
  bottom: 37.5%;
}
@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
