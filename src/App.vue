<script setup lang="ts">
import Heading from './components/Heading.vue';
import Character from './components/Character.vue';
import SubHeading from './components/SubHeading.vue';
const images = ['/src/assets/images/luke.jpeg', '/src/assets/images/vader.jpeg', 
'/src/assets/images/c3p0.jpeg', '/src/assets/images/R2D2.jpeg'];
</script>

<template>
  <main className = "page page--space">
    <Heading title="Star Wars" />
    <SubHeading text="A long time ago in a galaxy far, far away...." />
        <section className ="page__container">
        <Suspense>
          <Character v-for="(image, index) in images" :image ="image" :key="index"/>
        </Suspense>
        </section>
        </main>
</template>
