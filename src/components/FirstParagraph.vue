<script setup>
const props = defineProps({
  gender: {
    type: String,
    required: true,
  },
  age: {
    type: Number,
    required: true,
  },
  job: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <p>{{ gender === 'female' ? 'She' : 'He' }} is a {{ age }}-year-old {{ job.toLowerCase() }}.</p>
</template>

<style scoped></style>
