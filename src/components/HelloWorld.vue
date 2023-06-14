<script setup lang="ts">
import { ipcRenderer } from 'electron'
const props = defineProps<{ name: string, exe: string, icon: string }>()

//<slot></slot>const imageUrl = new URL(props.icon, import.meta.url).href

const run = (exe:string) => {
  ipcRenderer.send('run', exe)
}
</script>

<template>
  <div class="app" @click="run(exe)">
    <slot></slot>
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
