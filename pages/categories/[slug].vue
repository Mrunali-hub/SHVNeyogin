<script setup>

const route=useRoute();
</script>
<template>
    <h1>Example:{{ route.params.slug }}</h1>
</template>