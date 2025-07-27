<script setup>
const props = defineProps({
  firstname: {
    type: String,
    required: true,
  },
  lastname: {
    type: String,
    required: true,
  },
  gender: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <h2 :class="{ isFemale: gender === 'female' }">{{ firstname }} {{ lastname }}</h2>
</template>

<style scoped>
.isFemale {
  color: orange;
}
</style>
