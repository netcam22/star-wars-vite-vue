<script setup lang="ts">
defineProps<{ msg: string }>()

</script>

<template>
    <h1 className = "page__heading page__heading--gold">{{ msg }}</h1>
</template>
