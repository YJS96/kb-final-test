<script setup lang="ts">
import { onMounted } from 'vue'
import { useThemeStore } from '@/stores/theme'

import Main from '@/components/Main.vue'

onMounted(() => {
  const themeStore = useThemeStore()
  themeStore.setThemeColor('#FDFDFD')
})
</script>

<template>
  <Main :bg-gray="false">Medicine</Main>
</template>

<style scoped></style>
