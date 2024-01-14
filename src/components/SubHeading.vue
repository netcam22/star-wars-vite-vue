<script setup lang="ts">
defineProps<{ text: string }>()
</script>

<template>
    <h2 className = "page__sub-heading page__sub-heading--lavendar">{{text}}</h2>
</template>