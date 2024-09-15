<script setup lang="ts">
import { onMounted } from 'vue'
import { useThemeStore } from '@/stores/theme.ts'

const themeStore = useThemeStore()

onMounted(() => {
  themeStore.setThemeColor('#FDFDFD')
})
</script>

<template>
  <div>Medicine</div>
</template>

<style scoped></style>
