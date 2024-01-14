<script setup lang="ts">
defineProps<{ image: any, name: string, height: string}>();
async function fetchData() {
  try {
    const response = await fetch("https://swapi.dev/api/people/3");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}
fetchData();
</script>

<template>
  <div className = "card card--planet">
    <h2 className = "card__heading card__heading--darker-blue card__heading--gold-shadow-border">{{name}}</h2>
    <img v-bind:src="image" className = "card__image card__image--darker-blue" alt = "luke" />
    <p className = "card__text card__text--darker-blue card__text--gold-shadow-border">Height: {{height}}</p>
  </div>
</template>