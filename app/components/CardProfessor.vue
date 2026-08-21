<script setup lang="ts">

const props = defineProps<{
  foto: string      
  nome: string
  cargo: string
  linkedin: string  
}>()

</script>

<template>
    <div class="flex w-44 flex-col items-center text-center">
        <img :src="foto" class="mb-4 h-32 w-32 rounded-full object-cover" />
        <h3 class="rounded-xl bg-orange-500 pt-3 pr-8 pb-3 pl-6 text-[10px] font-medium text-white">{{ nome }}</h3>
        <p class="mt-4 text-xs text-gray-600">{{ cargo }} </p>
        <a :href="linkedin" target="_blank">
            <Icon class="mt-6 bg-orange-500 max-h-full" name="mdi:linkedin"/>
        </a>
    </div>

</template>