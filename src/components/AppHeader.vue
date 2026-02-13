<template>
    <header class="container">
        <h1 class="text-center my-5 display-1 fw-medium text-primary-emphasis">{{ titulo }}</h1>
    </header>
</template>

<script setup>
    import {ref} from 'vue'
    const titulo = ref("Restaurantcito")
</script>