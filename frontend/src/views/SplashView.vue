<script setup lang="ts">
import { APP_TITLE, APP_VERSION } from '@/utils/env'
</script>

<template>
  <div class="h-full flex flex-col items-center justify-center" style="--wails-draggable: drag">
    <img src="@/assets/logo.png" class="w-128" draggable="false" />
    <div class="text-24 font-bold mt-16 mb-24">{{ APP_TITLE }}</div>
    <div class="py-16">{{ APP_VERSION }}</div>
    <div class="progress">
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.progress {
  animation: rotate 2s infinite linear;
}
</style>
