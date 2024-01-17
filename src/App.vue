<script setup lang="ts">
import Heading from './components/Heading.vue';
import SubHeading from './components/SubHeading.vue';
import CharacterContainer from './components/CharacterContainer.vue';
</script>

<template>
  
  <main className = "page page--space">
    <Heading title="Star Wars" />
    <SubHeading text="A long time ago in a galaxy far, far away...." />
        <CharacterContainer />
    </main>
</template>
