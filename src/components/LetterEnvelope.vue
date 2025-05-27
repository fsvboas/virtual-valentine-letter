<script setup lang="ts">
import { ref } from 'vue'

const isEnvelopeOpen = ref(false)
const isLetterLifted = ref(false)

const toggleEnvelope = () => {
  if (!isEnvelopeOpen.value) {
    isEnvelopeOpen.value = true
    setTimeout(() => {
      isLetterLifted.value = true
    }, 300)
  }
}
</script>

<template>
  <div
    class="flex bg-[#ffe4c7] w-[300px] h-[200px] relative cursor-pointer justify-center shadow-2xl"
    @click="toggleEnvelope"
  >
    <div
      :class="[
        'w-0 h-0 border-l-[150px] border-l-transparent border-r-[150px] border-r-transparent border-b-[116px] border-b-[#ffe4c7]',
        'absolute z-10',
        isEnvelopeOpen ? 'rotate-0 -mt-[115px]' : 'rotate-180 z-50',
      ]"
    />
    <div
      className="w-0 h-0 border-t-[100px] border-t-transparent border-b-[100px] border-b-transparent border-r-[150px] border-r-[#f8cfa3] z-30 absolute right-0"
    />
    <div
      className="w-0 h-0 border-l-[150px] border-l-transparent border-r-[150px] border-r-transparent border-b-[100px] border-b-[#ebb983] absolute bottom-0 z-30"
    />
    <div
      className="w-0 h-0 border-t-[100px] border-t-transparent border-b-[100px] border-b-transparent border-l-[150px] border-l-[#f8cfa3] z-30 absolute left-0"
    />
    <div
      @click="toggleEnvelope"
      :class="[
        'w-[95%] h-full bg-white overflow-hidden absolute duration-300',
        isEnvelopeOpen ? 'z-20' : 'z-0',
        isLetterLifted ? '-mt-20' : '0',
      ]"
    >
      <p class="text-center p-4">
        lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem
        ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum
        lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem
        ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum
        lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem ipsum lorem
      </p>
    </div>
  </div>
</template>
