<script setup lang="ts">

import { publicoAlvo } from '~/data/publicoAlvo'
import { modulos } from '~/data/modulos'
import { resultados } from '~/data/resultados'
import { professores } from '~/data/professores'


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
    id="treinamento"
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
  class="relative mt-10 flex min-h-screen rounded-t-[50%_300px] items-start bg-[url('/fundoSecoes.png')] bg-cover bg-center px-6 pt-28"
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
    id="metodologia"
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
    class="relative mt-5 flex min-h-screen items-start bg-[url('/fundoSecoes.png')] bg-center px-6 pt-28">
    <div class="mx-auto max-w-7xl text-center  ">
    <h2 class="font-poppins mb-6 text-blue-500 text-xl font-extrabold sm:text-xl md:text-xl">
          Resultados Esperados
        </h2>
       <p class="font-lato mt-4 text-xs text-gray-300"> Ao final do treinamento, você estará preparado para:</p>

       <div class="mt-10 flex flex-wrap justify-center gap-6 text-orange-500 p-2">
         <CardInfo
           v-for="item in resultados"
           :key="item.titulo"
           tipo="resultados"
           :icon="item.icon"
           :titulo="item.titulo"
           :conteudo="item.conteudo"
         />
       </div>
       <span class="rounded-xl bg-orange-500 pt-3 pr-8 pb-3 pl-6 text-xs font-medium text-white  "
            >Sua pesquisa pode ser a próxima grande solução.</span>
    </div>
    </section>

    <section
    id="professores" class="bg-white px-8 py-8">
      <div class="mx-auto max-w-7xl text-center">
        <h2
          class="font-poppins mb-6 text-blue-900 text-xl font-extrabold sm:text-xl md:text-xl">
          Conheça os Professores
        </h2>
      </div>
      <!-- Fileira de cima: 4 professores -->
      <div class="mt-20 mx-auto flex max-w-7xl flex-wrap justify-center gap-8">
        <CardProfessor
          v-for="prof in professores.slice(0, 4)"
          :key="prof.nome"
          :foto="prof.foto"
          :nome="prof.nome"
          :cargo="prof.cargo"
          :linkedin="prof.linkedin"
        />
      </div>

      <!-- Fileira de baixo: do 5º em diante -->
      <div class="mx-auto mt-8 flex max-w-7xl flex-wrap justify-center gap-8">
        <CardProfessor
          v-for="prof in professores.slice(4)"
          :key="prof.nome"
          :foto="prof.foto"
          :nome="prof.nome"
          :cargo="prof.cargo"
          :linkedin="prof.linkedin"
        />
      </div>
      
        

    </section>

    <!-- ===== SEÇÃO DE CADASTRO ===== -->
    <section id="cadastro" 
    class="relative overflow-hidden bg-white px-8 py-24   ">

      <!-- wrapper do card: 'relative' = o "palco" pro brilho se posicionar -->
      <div class="relative mx-auto max-w-4xl">

        <!-- CAMADA 1: brilho laranja (maior que o card, atrás dele) -->
        <div
        id="CamadaTranslucida"
          class="pointer-events-none absolute left-2/3 -top-2/4 h-[80%] w-[300%] -translate-x-1/2 translate-y-1/4 bg-orange-400 opacity-50 blur-lg "
        ></div>

        <!-- CAMADA 2: o card principal ('z-10' = na frente do brilho) -->
        <div 
        id="imagemFundo"
        class="relative z-10 rounded-3xl bg-[url('/fundoSecoes.png')] bg-center px-6 pt-28 p-8 text-center shadow-2xl sm:p-12">

          <!-- 1. Badge -->
          <span
            class="inline-block rounded-[5px] border-2 border-orange-500 px-5 py-2 text-sm font-bold text-orange-500"
          >
            Não deixe sua pesquisa parar no laboratório.
          </span>

          
          <h2 class="mt-6 text-2xl font-bold text-white sm:text-lg">
            Cadastre-se para a <span class="text-orange-500">4º edição</span> e receba todas as
            informações sobre o treinamento
          </h2>
          <p class="mx-auto mt-4 max-w-2xl text-xs font-normal text-white/80">
            Participe do <span class="font-bold">Treinamento de Empreendedorismo para Cientistas</span>
            e descubra como transformar conhecimento em impacto.
          </p>

          <!-- 3. Aqui vai o SEU componente do formulário: -->
          <!-- <FormularioCadastro /> -->
          <div
          id="formulario" 
          class=" rounded-lg text-sm text-white/40">
         <Formulario />
          </div>

        </div>
    </div>
    </section>
    <section>
         <div class="mx-auto mt-16 grid max-w-4xl grid-cols-1 gap-8 text-center sm:grid-cols-2">
        <h3
          class="bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-3xl font-extrabold text-transparent"
        >
          Apoio
        </h3>
        <h3
          class="bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-3xl font-extrabold text-transparent"
        >
          Patrocinadores
        </h3>
      </div>
      <h3
          class="text-center bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-3xl font-extrabold text-transparent p-20"
        >
          Unidades de Pesquisa Vinculados
    </h3>
    </section>


</template>
