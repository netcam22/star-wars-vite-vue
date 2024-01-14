<script setup lang="ts">
import Heading from './components/Heading.vue';
import Character from './components/Character.vue';
</script>

<template>
  <main className = "page page--space">
    <Heading msg="Star Wars" />
        <h2 className = "page__sub-heading page__sub-heading--lavendar">A long time ago in a galaxy far, far away....</h2>
        <section className ="page__container">
          <Character />
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
