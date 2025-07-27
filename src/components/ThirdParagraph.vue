<script setup>
const props = defineProps({
  gender: {
    type: String,
    required: true,
  },
  pet: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <p>
    At home, {{ gender === 'female' ? 'her' : 'his' }} lively companion is {{ pet.name }} a
    {{ pet.age }}-years-old {{ pet.species }}.
  </p>
</template>
