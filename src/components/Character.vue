<script setup lang="ts">

defineProps<{ image: any}>();
async function fetchData() {
  try {
    const response = await fetch("https://swapi.dev/api/people/3");
    const json = await response.json();
    return json;
  } catch (error) {
    console.error(error);
  }
}
const data = await fetchData();
</script>

<template>
  <div className = "card card--planet">
    <h2 className = "card__heading card__heading--darker-blue card__heading--gold-shadow-border">{{data.name}}</h2>
    <img v-bind:src="image" className = "card__image card__image--darker-blue" alt = "luke" />
    <p className = "card__text card__text--darker-blue card__text--gold-shadow-border">Height: {{data.height}}</p>
  </div>
</template>