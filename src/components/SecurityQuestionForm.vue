<script setup lang="ts">
import { ref } from 'vue'
const inputValue = ref<string>('')
</script>

<template>
  <div class="flex flex-col w-full h-fit p-4 bg-white border-2 border-[#f8cfa3] rounded space-y-2">
    <span class="text-sm text-center"
      >Antes de continuar, confirme que esta carta é para você.</span
    >
    <form @submit.prevent="">
      <label class="text-xs">Em qual dia nos conhecemos?</label>
      <div class="flex flex-row space-x-2">
        <input
          v-model="inputValue"
          class="bg-white border-2 border-[#f8cfa3] w-full p-1 rounded-md"
          type="text"
        />
        <button type="submit" class="bg-[#f8cfa3] p-2 rounded-md hover:cursor-pointer text-sm">
          Validar
        </button>
      </div>
    </form>
  </div>
</template>
