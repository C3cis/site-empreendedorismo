<script setup lang="ts">
defineProps<{
  tipo: string
  icon: string
  titulo: string
  conteudo: string
}>()
</script>

<template>
  <div
    class="rounded-[11px] p-3"
    :class="{
      'w-[154px] h-[176px] border-4 border-orange-500 bg-white': tipo === 'publicoAlvo',

      'w-[260px] h-[125px] border-4 border-orange-600 bg-black/20 flex flex-row ': tipo === 'modulo',

      'h-[143px] w-[285px] bg-transparent': tipo === 'resultados',
    }"
  >
    <Icon :name="icon" class="mb-4 text-6xl" />
    <h3 class="text-xl font-bold">{{ titulo }}</h3>
    <p class="mt-2 text-gray-700">{{ conteudo }}</p>
  </div>
</template>
