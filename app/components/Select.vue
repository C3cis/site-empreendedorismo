<script setup lang="ts">
// Igual ao Input, mas com uma prop a mais: 'opcoes' (a lista do dropdown).
defineProps({
  id: { type: String, required: true },
  label: { type: String, default: '' },
  placeholder: { type: String, default: '' },
  // as opções vêm de FORA (do Formulario). PropType diz que é uma lista de textos.
  opcoes: { type: Array as PropType<string[]>, required: true },
  required: { type: Boolean, default: true },
})

// mesmo v-model do Input
const model = defineModel<string>()
</script>

<template>
  <div>
    <label :for="id" class="mb-1 block text-sm font-medium text-white">
      {{ label }}
      <span v-if="required" class="text-red-500">*</span>
    </label>

    <select
      :id="id"
      v-model="model"
      :required="required"
      class="w-full rounded-lg border border-white/20 bg-white/10 px-4 py-2 text-white focus:border-orange-500 focus:outline-none"
    >
      <!-- Selects não têm "placeholder": a gente finge com uma opção vazia e disabled -->
      <option value="" disabled>{{ placeholder }}</option>

      <!-- Cada opção da lista vira um <option>. v-for igual ao dos cards! -->
      <option v-for="op in opcoes" :key="op" :value="op">{{ op }}</option>
    </select>
  </div>
</template>
