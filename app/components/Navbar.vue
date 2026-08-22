<script setup lang="ts">
const navLinks = [
  { name: 'Treinamento', to: '/#treinamento' },
  { name: 'Público-alvo', to: '/#publicoAlvo' },
  { name: 'Conteúdo', to: '/#conteudo' },
  { name: 'Metodologia', to: '/#metodologia' },
  { name: 'Resultado', to: '/#resultado' },
  { name: 'Professores', to: '/#professores' },
  { name: 'Edições anteriores', to: '/#depoimentos' },
]
</script>

<template>
  <header class="absolute inset-x-0 top-0 z-50 border-b border-orange-500 backdrop-blur ">

    <div class="flex max-w-3xl items-center justify-between px-16 py-4 mx-auto">

        <div class="flex items-center gap-2"> 
      <img src="/nit.png" alt="Logo" class="h-7 w-auto"/>
      <img src="/logoGov.png" alt="Logo" class="h-7 w-auto" />
        </div>
       

      <nav class="hidden gap-5 md:flex">
        <NuxtLink
          v-for="link in navLinks"
          :key="link.to"
          :to="link.to"
          class="text-[10px] font-medium text-gray-200 transition hover:text-blue-900"
        >
          {{ link.name }}
        </NuxtLink>
      </nav>
    </div>
  </header>
</template>
