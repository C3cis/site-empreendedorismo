<script setup lang="ts">
defineProps({
  id: { type: String, required: true },
  label: { type: String, default: '' },
  placeholder: { type: String, default: '' },
  opcoes: { type: Array as PropType<string[]>, required: true },
  required: { type: Boolean, default: true },
})

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
      <option value="" disabled>{{ placeholder }}</option>

      <option v-for="op in opcoes" :key="op" :value="op">{{ op }}</option>
    </select>
  </div>
</template>
