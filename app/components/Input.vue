<script setup lang="ts">
// Props que o formulário passa pra cada campo (estilo runtime, igual ao da equipe)
defineProps({
  id: { type: String, required: true }, // liga a <label> ao <input>
  type: { type: String, default: 'text' }, // text | email | tel...
  label: { type: String, default: '' }, // texto que aparece em cima
  placeholder: { type: String, default: '' }, // texto "fantasma" dentro do campo
  autocomplete: { type: String, default: '' },
  required: { type: Boolean, default: true }, // mostra o "*" e valida
})

// defineModel() = faz este componente aceitar v-model.
// "model" é uma variável reativa ligada ao v-model do pai (mão dupla).
const model = defineModel<string>()
</script>

<template>
  <div>
    <!-- Label ligada ao input pelo id (clicar nela foca o campo = acessibilidade) -->
    <label :for="id" class="mb-1 block text-sm font-medium text-white">
      {{ label }}
      <span v-if="required" class="text-red-500">*</span>
    </label>

    <!-- O input de verdade. v-model="model" conecta o que é digitado ao defineModel. -->
    <input
      :id="id"
      v-model="model"
      :type="type"
      :placeholder="placeholder"
      :autocomplete="autocomplete"
      :required="required"
      class="w-full rounded-lg border border-white/20 bg-white/10 px-4 py-2 text-white placeholder-white/50 focus:border-orange-500 focus:outline-none"
    />
  </div>
</template>
