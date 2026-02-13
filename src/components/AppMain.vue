<template>
    <main>
        <div class="container mb-5">
            <ToggleButton texto="Ver Seccion" @toggle="mostrar = !mostrar" />
            <ToggleSection 
                v-if="mostrar"
            />
        </div>
        <section class="container mb-5">
            <h2 class="text-center my-5 display-5 fw-normal">{{subtitulo}}</h2>
            <div class="row gap-5 justify-content-evenly">
                <!-- Aqui deberian ir las tarjetas -->
                <!-- <Card /> -->
                <div class="col-10 col-sm-10 col-md-5 col-lg-3"
                    v-for="card in cards"
                    :key="card.id"
                >
                    <Card
                        :imagen="card.imagen"
                        :titulo="card.titulo"
                        :descripcion="card.descripcion"
                    />
                </div>
            </div>
        </section>
        <Payment />
    </main>
</template>

<script setup>
    import { ref } from 'vue';
    import Payment from './Payment.vue';
    import Card from './Card.vue';
    const subtitulo = ref('Nuestros Platos')

    //Importar imagenes
    import bebidas from '@/assets/img/bebidas.jpg'
    import colaciones from '@/assets/img/colaciones.jpg'
    import desayunos from '@/assets/img/desayunos.jpg'
    import dulces from '@/assets/img/dulces.jpg'
    import empanadas from '@/assets/img/empanadas.jpg'
    import verduras from '@/assets/img/verduras.jpg'
    import ToggleButton from './ToggleButton.vue';
    import ToggleSection from './ToggleSection.vue';

    const cards = ref([
        {
            id: 1,
            titulo: "Bebidas",
            descripcion: "Tomate una rica bebida para el calor",
            imagen: bebidas
        },
        {
            id: 2,
            titulo: "Colaciones",
            descripcion: "Almuerza con nosotros una de nuestas contundentes colaciones.",
            imagen: colaciones
        },
        {
            id: 3,
            titulo: "Desayunos",
            descripcion: "Comienza el día con un tremendo desayuno!",
            imagen: desayunos
        },
        {
            id: 4,
            titulo: "Dulces",
            descripcion: "Los mejores dulces de la zona",
            imagen: dulces
        },
        {
            id: 5,
            titulo: "Empanadas",
            descripcion: "Las empanadas más premiadas de la región!",
            imagen: empanadas
        },
        {
            id: 6,
            titulo: "Verduras",
            descripcion: "A nadie le gustan las verduras, pero aquí nos queda espectaculares!",
            imagen: verduras
        },
        {
            id: 7,
            titulo: "Nuevo Plato",
            descripcion: "Nueva adicion a nuestro menu!",
            imagen: colaciones
        },
    ])
    
    const mostrar = ref(false)
</script>