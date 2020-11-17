<template>
<div class="about">
    <Inicio />
</div>
</template>

<script>
import Inicio from '@/components/Inicio.vue'

export default {
    name: 'About',
    components: {
        Inicio
    }
}
</script>

<style>
.about {
    height: 100vh;
    background-image: url(../assets/ciuTres.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;
}
</style>
