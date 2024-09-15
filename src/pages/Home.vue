<script setup lang="ts">
import { onMounted } from 'vue'
import { useThemeStore } from '@/stores/theme'

const themeStore = useThemeStore()

onMounted(() => {
  themeStore.setThemeColor('#F6F7F6')
})
</script>

<template>
  <div>Home</div>
</template>

<style scoped></style>
