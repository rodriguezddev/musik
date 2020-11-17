<template>
<div class="inicioRe">
    <Canciones />
</div>
</template>

<script>
import Canciones from '@/components/Canciones.vue'

export default {
    name: 'InicioRe',
    components: {
        Canciones
    }
}
</script>

<style>
.inicioRe {
    background-image: url(../assets/ciuCinco.jpg);
    background-size: cover;
    background-position: center center;
}
</style>
