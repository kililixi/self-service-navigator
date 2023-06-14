<script setup lang="ts">
import { ipcRenderer } from 'electron'
defineProps<{ name: string, exe: string, icon: string }>()

const run = (exe:string) => {
  ipcRenderer.send('run', exe)
}
</script>

<template>
  <div class="app" @click="run(exe)">
    <img :src="icon" class="logo electron" :alt="name" />
    <span>{{ name }}</span>
  </div>

</template>

<style scoped>
.read-the-docs {
  color: #888;
}
.app {
  display: flex;
  flex: 1;
  flex-direction: column;
  align-items: center;
}
</style>
