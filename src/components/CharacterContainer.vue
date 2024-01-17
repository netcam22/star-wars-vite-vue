<script setup lang="ts">
const characters = [{id: '1', image: '/src/assets/images/luke.jpeg'}, 
{id: '4', image: '/src/assets/images/vader.jpeg'}, 
{id: '2', image: '/src/assets/images/c3p0.jpeg'}, 
{id: '3', image: '/src/assets/images/R2D2.jpeg'}];

import Character from "./Character.vue";

</script>

<template>

<section className ="page__container">
    <Character v-for="(character) in characters"
    :key="character.id" 
    :image="character.image" :characterId="character.id" />
</section>
</template>