<script setup lang="ts">
const props = defineProps<{
  tipo: string
  icon: string
  titulo: string
  conteudo: string
}>()


const horizontal = props.tipo === 'modulo' || props.tipo === 'aula'

</script>

<template>
  <div
    class="flex"
    :class="{
      'h-[176px] w-[154px] rounded-[11px] border-4 border-orange-500 bg-white p-3 flex-col items-center text-center': tipo === 'publicoAlvo',

      'h-[125px] w-[260px] rounded-[11px] border-4 border-orange-600 bg-white/10 p-3 backdrop-blur-sm flex-wrap items-center gap-2 text-left': tipo === 'modulo',

      'h-[143px] w-[285px] rounded-[11px] bg-transparent p-3 flex-col items-center text-center': tipo === 'resultados',

      'rounded-[11px] border-2 border-orange-500 bg-white p-6 flex-wrap items-center gap-3 text-left': tipo === 'aula',
    }"
  >
    <Icon :name="icon" :class="horizontal ? 'text-2xl' : 'mb-4 text-2xl'" />
    <h3 class="font-bold" :class="horizontal ? 'text-sm p-2' : 'text-sm'">{{ titulo }}</h3>
    <p
      :class="{
        'mt-2 text-gray-700': tipo === 'publicoAlvo',
        'mt-2 text-gray-100 text-xs': tipo === 'resultados',
        'w-full text-xs text-gray-100': tipo === 'modulo',
        'w-full text-xs font-bold text-gray-900': tipo === 'aula',
      }"
    >
      {{ conteudo }}
    </p>
  </div>
</template>
