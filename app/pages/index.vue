<script setup lang="ts">

import { publicoAlvo } from '~/data/publicoAlvo'
import { modulos } from '~/data/modulos'


</script>

<template>
    <section
      id="HeroBanner"
      class="relative flex min-h-screen w-full items-start bg-[url('/fundoHero.png')] bg-cover bg-center px-6 pt-28 " >

      <article class="grid gap-6 text-left">
        <div class="mx-auto px-6  max-w-3xl">
          <span class="rounded-3xl bg-orange-500 pt-3 pr-4 pb-3 pl-6 text-xs font-medium text-white"
            >3ª EDIÇÃO - INSCRIÇÕES ENCERRADAS!</span>
             <h1
            class="font-poppins mt-4 text-6xl leading-tight font-extrabold text-cyan-400 ">
            Transforme sua pesquisa em
            <span class="text-orange-500">inovação</span>
          </h1>
          <p class="font-lato mt-5 text-base text-gray-200  md:text-sm">
            Treinamento de Empreendedorismo para Cientistas – uma <br class="hidden md:block" />
            imersão prática de
            <span class="font-bold text-white">32 horas</span> para transformar descobertas
            <br class="hidden md:block" />
            científicas em soluções com impacto real.
          </p>
          <button
            class="mt-6 rounded-lg bg-orange-500 px-3 py-2 text-xs font-medium text-white transition hover:bg-orange-600 mb-9"> Quero Participar! </button>
        </div>
      </article>
    </section>

    <section 
    id="Treinamento"
    class="relative bg-white px-3 py-8">
   <div class="grid grid-cols-1  mx-auto max-w-3xl text-center ">
        <h2
          class="font-poppins mb-6 text-blue-900 text-xl font-extrabold sm:text-xl md:text-xl">
          Sobre o Treinamento
        </h2>
        <p class="font-lato text-xs text-gray-700">
          A ciência brasileira gera conhecimento de ponta, mas muitas vezes esse potencial não chega
          à sociedade. Este treinamento foi criado para mudar isso.
          <br />
          Com <span class="font-bold text-gray-900">32 horas de aulas e apresentação final</span>,
          você vai desenvolver competências empreendedoras, estruturar projetos de base científica e
          se conectar a oportunidades de editais e parcerias como o
          <span class="font-bold text-orange-500">InScience+</span>.
        </p>
    </div>
    </section>
    <section
    id="publicoAlvo" class="bg-white px-8 py-8">
      <div class="mx-auto max-w-7xl text-center">
        <h2
          class="font-poppins mb-6 text-blue-900 text-xl font-extrabold sm:text-xl md:text-xl">
          Público-alvo
        </h2>
        <p class="font-lato mt-4 text-xs text-gray-600">Este programa é feito para:</p>
      </div>
      <div class="mt-10 flex flex-wrap justify-center gap-32 text-orange-500 text-center">
        <CardInfo
            v-for="item in publicoAlvo"
            :key="item.titulo"
            tipo="publicoAlvo"
            :icon="item.icon"
            :titulo="item.titulo"
            :conteudo="item.conteudo"
        />
</div>
    </section>

    <section
   id="conteudo"
  class="relative mt-10 flex min-h-screen rounded-t-[50%_300px] items-start bg-[url('/fundoSecao3.png')] bg-cover bg-center px-6 pt-28"
    >
    <div class="mx-auto max-w-7xl text-center">
        <h2 class="font-poppins mb-6 text-blue-400 text-xl font-extrabold sm:text-xl md:text-xl">
            O que você vai aprender?
        </h2> 
        <p class="font-lato mt-4 text-xs text-gray-300"> Durante o treinamento, você passará por módulos que combinam
          <span class="font-semibold text-orange-400"> teoria e prática</span>:
        </p>

        <div class="mx-auto mt-10 grid w-fit grid-flow-col grid-rows-4 gap-6 ">
          <CardInfo
            v-for="item in modulos"
            :key="item.titulo"
            tipo="modulo"
            :icon="item.icon"
            :titulo="item.titulo"
            :conteudo="item.conteudo"
          />
        </div>
    </div>


    </section>

</template>
