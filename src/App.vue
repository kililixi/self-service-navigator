<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'

</script>

<template>
  <div> <h1>{{ '请根据要办理的业务进入对应的程序。' }}</h1></div>
  <div style="display: flex;">
    <HelloWorld name="程序1" icon="/src/assets/electron.svg" exe="F:\Fiddler\Fiddler.exe" />
    <HelloWorld name="程序2" icon="/src/assets/vite.svg" exe="aaa" />
    <HelloWorld name="程序3" icon="/src/assets/vue.svg" exe="aaa" />
  </div>
  
</template>

<style>
.flex-center {
  display: flex;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 6em;
  width: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo.electron:hover {
  filter: drop-shadow(0 0 2em #9FEAF9);
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

</style>
