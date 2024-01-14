<script setup lang="ts">
import Heading from './components/Heading.vue';
import Character from './components/Character.vue';
import SubHeading from './components/SubHeading.vue';
</script>

<template>
  <main className = "page page--space">
    <Heading title="Star Wars" />
    <SubHeading text="A long time ago in a galaxy far, far away...." />
        <section className ="page__container">
        <Character image = './assets/images/luke.jpeg' />
        <Character image = './assets/images/vader.jpeg' />
        <Character image = './assets/images/c3p0.jpeg' />
        <Character image = './assets/images/R2D2.jpeg' />
        </section>
        </main>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
