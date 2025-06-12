<script setup lang="ts">
import { useLetterModalStore } from '@/stores/useLetterModalStore'
import { X } from 'lucide-vue-next'

const letterModalStore = useLetterModalStore()
</script>

<template>
  <div class="bg-white absolute z-70 max-w-[500px] h-fit p-4 flex flex-col">
    <button
      class="flex self-end cursor-pointer hover:text-red-500 duration-200 p-px"
      @click="letterModalStore.closeModal"
    >
      <X />
    </button>
    <p class="text-justify p-4 max-md:text-sm">
      Yasmin,
      <br />
      <br />
      Esse é o nosso primeiro dia dos namorados. É o meu primeiro da vida, honestamente, mas eu não
      poderia estar mais contente. Sou imensamente grato por ter te conhecido, ter você ao meu lado
      é, de longe, a minha maior realização dos últimos anos.
      <br />
      <br />
      Seu jeitinho, sua alegria e sua força de vontade me motiva todos os dias. Me faz querer ser
      mais, me faz querer correr atrás dos meus próprios objetivos. Algumas coisas que eu já até
      havia desistido, mas que depois de te conhecer, me fez querer correr atrás novamente.
      <br />
      <br />
      Espero que a nossa história continue a se desenrolar com muitos momentos felizes, e que nunca
      nos falte força para enfrentarmos juntos qualquer desafio que surgir.
      <br />
      <br />
      Minha gatinha, saiba que torço por você todos os dias. Conte comigo para qualquer coisa na sua
      vida. Farei de tudo para estar aqui, sempre ao seu lado.
      <br />
      <br />
      <span class="text-2xl text-red-700">Eu te amo!</span>
    </p>
  </div>
</template>
