<template>
  <span class="message"> {{message}} </span>
</template>

<script setup>
const props = defineProps({
  message: String
});
</script>

<style>

</style>