<script setup lang="ts">
const year = new Date().getFullYear()

const redes = [
  { nome: 'Facebook', url: 'https://www.facebook.com/nitriomcti/', icon: 'mdi:facebook' },
  { nome: 'Instagram', url: 'https://www.instagram.com/nitriomcti', icon: 'mdi:instagram' },
  { nome: 'LinkedIn', url: 'https://www.linkedin.com/company/nitriomcti/', icon: 'mdi:linkedin' },
  { nome: 'YouTube', url: 'https://www.youtube.com/@nitriomcti', icon: 'mdi:youtube' },
  { nome: 'X', url: 'https://x.com/nitriomcti/', icon: 'ri:twitter-x-fill' },
]
</script>

<template>
  <footer class="bg-[#212951] py-8 text-center text-white">
    <p class="mb-4 text-xs font-poppins">
      © 2007 - {{ year }} Todos os direitos reservados <br />
      Ministério da Ciência, Tecnologia e Inovação - MCTI
    </p>

    <div class="flex justify-center gap-6 p-2 text-2xl">
      <NuxtLink
        v-for="rede in redes"
        :key="rede.nome"
        :to="rede.url"
        external
        target="_blank"
        :aria-label="rede.nome"
        class="text-gray-400 transition hover:text-white"
      >
        <Icon :name="rede.icon" />
      </NuxtLink>
    </div>
  </footer>
</template>
