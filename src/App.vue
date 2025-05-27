<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <div
    class="flex flex-col min-h-screen w-full bg-[url(../../public/image-background.webp)] bg-cover bg-no-repeat font-medium"
  >
    <RouterView />
  </div>
</template>
