<script setup lang="ts">
defineProps<{ image: any }>();
</script>

<template>
  <div className = "card card--planet">
    <img v-bind:src="image" className = "card__image card__image--darker-blue" alt = "luke" />
  </div>
</template>
