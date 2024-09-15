<script setup lang="ts">
import { onMounted } from 'vue'
import { useThemeStore } from '@/stores/theme'

import Main from '@/components/Main.vue'

onMounted(() => {
  const themeStore = useThemeStore()
  themeStore.setThemeColor('#F6F7F6')
})
</script>

<template>
  <Main :bg-gray="true">Home</Main>
</template>

<style scoped></style>
