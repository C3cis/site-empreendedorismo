<script setup lang="ts">

import { publicoAlvo } from '~/data/publicoAlvo'
import { modulos } from '~/data/modulos'
import { resultados } from '~/data/resultados'


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

        <div class="mx-auto mt-20 grid w-fit grid-flow-col grid-rows-4 gap-8 text-orange-500 text-center">
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

    <section
    id="metologia"
    class="bg-white px-8 py-8">
    <div class="mx-auto max-w-7xl text-center">
    <h2 class="font-poppins mb-6 text-blue-900 text-xl font-extrabold sm:text-xl md:text-xl">
          Metologia
        </h2>
       <p class="font-lato mt-4 text-xs text-gray-700"> Um formato dinâmico <span class="font-bold text-gray-900">totalmente online.</span> <br/>  Tudo aplicado diretamente em 
          <span class="font-semibold text-orange-400"> projetos reais dos participantes</span>:
        </p>
    </div>

    <!-- Área do vídeo -->
    <div class="relative mx-auto mt-24 w-full max-w-xl">
      <img
        src="/componentes-visuais/ao vivo.png"
        alt="ao vivo"
        class="pointer-events-none absolute -top-20 -left-20 z-10 w-[240px] opacity-80"
      />
      <img
        src="/componentes-visuais/lives.png"
        alt="lives"
        class="pointer-events-none absolute top-1/2 -right-14 w-12 -translate-y-1/2 z-10"
      />
      <!--Quadrado e bolas do design-->

      <div id="quadrado"
      class="absolute -top-6 -left-6 h-24 w-32 rounded-3xl bg-orange-500"></div>

      <div id="bola-1"
      class="absolute -bottom-10  -right-10 h-40 w-40 rounded-full bg-orange-400 blur-sm"></div>

      <div id="bola-2" 
      class="absolute bottom-3 -right-20 h-40 w-40  rounded-full bg-orange-400 opacity-60 blur-sm"></div>

      <div id="video"
      class="relative z-10 overflow-hidden rounded-3xl border-2 border-blue-400">
        <img src="/componentes-visuais/videoAula.png" alt="Aula ao vivo" class="w-full" />
      </div>

      <div
        id="aviso"
        class="absolute -top-10 right-2 z-20 flex items-center gap-1 rounded-full border border-orange-500 bg-white px-4 py-1 text-xs font-medium text-gray-700 shadow" >
        <Icon name="mdi:alert" class="text-sm text-orange-500" />
        As aulas não ficarão gravadas
      </div>
    </div>

    <div class="mx-auto mt-8 grid max-w-xl grid-cols-2 gap-16 text-orange-500">
      <CardInfo
        tipo="aula"
        icon="mdi:calendar"
        titulo="Início das Aulas"
        conteudo="00 de mês de 0000"
      />
      <CardInfo
        tipo="aula"
        icon="mdi:clock-outline"
        titulo="Dia e Horário"
        conteudo="Seg a Sex · 19h–22h"
      />
    </div>
    </section>

    <section
    id="resultado"
    class="relative mt-5 flex min-h-screen items-start bg-[url('/fundoSecao3.png')] bg-center px-6 pt-28">
    <div class="mx-auto max-w-7xl text-center ">
    <h2 class="font-poppins mb-6 text-blue-500 text-xl font-extrabold sm:text-xl md:text-xl">
          Resultados Esperados
        </h2>
       <p class="font-lato mt-4 text-xs text-gray-300"> Ao final do treinamento, você estará preparado para:</p>

       <div class="mt-10 flex flex-wrap justify-center gap-6 text-orange-500">
         <CardInfo
           v-for="item in resultados"
           :key="item.titulo"
           tipo="resultados"
           :icon="item.icon"
           :titulo="item.titulo"
           :conteudo="item.conteudo"
         />
       </div>
    </div>
    </section>
    

</template>
