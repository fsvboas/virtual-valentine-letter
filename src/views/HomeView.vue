<script setup lang="ts">
import LetterEnvelope from '@/components/LetterEnvelope.vue'
import SecurityQuestionForm from '@/components/SecurityQuestionForm.vue'
</script>

<template>
  <main class="flex flex-col items-center justify-center min-h-screen h-full">
    <div class="flex flex-col justify-center items-center space-y-4 max-w-[300px]">
      <LetterEnvelope />
      <SecurityQuestionForm />
    </div>
  </main>
</template>
