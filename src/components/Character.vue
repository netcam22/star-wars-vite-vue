<script setup lang="ts">
defineProps<{ image: any, name: string}>();
</script>

<template>
  <div className = "card card--planet">
    <h2 className = "card__heading card__heading--darker-blue card__heading--gold-shadow-border">{{name}}</h2>
    <img v-bind:src="image" className = "card__image card__image--darker-blue" alt = "luke" />
  </div>
</template>