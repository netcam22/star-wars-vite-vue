<script setup lang="ts">

interface apiData {
    name: string,
    height: string
}

import { toRefs } from 'vue';
import { onBeforeMount, ref } from "vue";
import {useFetch} from './../hooks/useFetch';

const props = defineProps({image: String, characterId: String})
const { characterId, image } = toRefs(props)

const fetchingError = ref(false);
const swapiData = ref<apiData | null>();

onBeforeMount(async () => {
  if (characterId) {
    const {data, hasError} = await useFetch<apiData>(`https://swapi.dev/api/people/${characterId?.value}`);
  swapiData.value = data.value;
  fetchingError.value = hasError.value;
  }
});
</script>

<template>
<div v-if="fetchingError" className ="card card--planet">
  <h2 className = "card__heading card__heading--darker-blue card__heading--gold-shadow-border">Error: no data</h2>
</div> 
  <div v-if="swapiData" className = "card card--planet">
    <h2 className = "card__heading card__heading--darker-blue card__heading--gold-shadow-border">{{swapiData.name}}</h2>
    <img v-bind:src="image" className = "card__image card__image--darker-blue" alt = "luke" />
    <p className = "card__text card__text--darker-blue card__text--gold-shadow-border">Height: {{swapiData.height}}</p>
  </div>
</template>