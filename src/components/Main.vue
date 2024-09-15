<template>
  <div v-if="bgWhite" class="safe-area"></div>
  <div :class="padded ? 'padded main-frame ' : 'main-frame'" :style="{ backgroundColor: bgColor }">
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
import { computed, defineProps } from 'vue'

const props = defineProps({
  padded: {
    type: Boolean,
    default: false
  },
  bgWhite: {
    type: Boolean,
    default: false
  }
})

const bgColor = computed(() => (props.bgWhite ? 'var(--white)' : 'var(--background)'))
</script>

<style scoped>
.main-frame {
  background-color: var(--background);
  position: absolute;
  width: 100%;
  height: calc(100% - 76px);
  overflow-x: hidden;
  overflow-y: scroll;
}

.padded {
  padding: 0px 5.56%;
}

.safe-area {
  position: absolute;
  top: -env(safe-area-inset-top);
  height: env(safe-area-inset-top);
}
</style>
