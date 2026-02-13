<template>
    <div class="card  p-0">
        <img :src="imagen" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">{{ titulo }}</h5>
            <p class="card-text">{{ descripcion }}</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
    </div>
</template>

<script setup>
    defineProps({
        imagen: String,
        titulo: String,
        descripcion: String
    })
</script>