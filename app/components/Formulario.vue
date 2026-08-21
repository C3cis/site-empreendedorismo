<script setup lang="ts">
// As listas dos selects moram aqui (o pai), e são passadas pro <Select> via :opcoes
const opcoesFormacao = ['Graduação', 'Mestre', 'Doutor', 'Especialização']
const opcoesStatus = ['Pesquisador', 'Iniciação Científica', 'Mestrando', 'Doutorando', 'Pós-doc']

// state = um objeto reativo que guarda o valor de TODOS os campos.
// Cada v-model="state.xxx" preenche uma dessas propriedades.
const state = reactive({
  nome: '',
  email: '',
  whatsapp: '',
  formacao: '',
  status: '',
  instituicao: '',
})

// Por enquanto (só interface): só mostra no console.
// Depois, aqui entra o envio pro backend.
function inscreverse() {
  console.log('Dados do formulário:', state)
}
</script>

<template>
  <!-- .prevent impede o reload da página ao enviar -->
  <form class="mt-8 grid grid-cols-1 gap-6 md:grid-cols-3" @submit.prevent="inscreverse">
    <!-- Linha 1 -->
    <Input id="nome" v-model="state.nome" type="text" label="Nome" placeholder="Nome" />
    <Input id="email" v-model="state.email" type="email" label="E-mail" placeholder="E-mail" />
    <Input id="whatsapp" v-model="state.whatsapp" type="tel" label="Telefone / WhatsApp" placeholder="(xx) xxxxx-xxxx" />

    <!-- Linha 2 -->
    <Select id="formacao" v-model="state.formacao" label="Nível de Formação" placeholder="Selecione..." :opcoes="opcoesFormacao" />
    <Select id="status" v-model="state.status" label="Status" placeholder="Selecione..." :opcoes="opcoesStatus" />
    <Input id="instituicao" v-model="state.instituicao" type="text" label="Instituição a qual está vinculado" placeholder="Instituição" />

    <!-- Botão: ocupa as 3 colunas e centraliza -->
    <div class="flex justify-center md:col-span-3">
      <button
        type="submit"
        class="mt-4 rounded-lg bg-orange-500 px-10 py-3 font-bold text-white transition hover:bg-orange-600"
      >
        Cadastre-se
      </button>
    </div>
  </form>
</template>
