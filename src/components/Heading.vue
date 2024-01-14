<script setup lang="ts">
defineProps<{ title: string }>()
</script>

<template>
    <h1 className = "page__heading page__heading--gold">{{ title }}</h1>
</template>
