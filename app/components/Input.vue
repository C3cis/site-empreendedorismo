<script setup lang="ts">
defineProps({
  id: { type: String, required: true }, 
  type: { type: String, default: 'text' }, 
  label: { type: String, default: '' }, 
  placeholder: { type: String, default: '' }, 
  autocomplete: { type: String, default: '' },
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
