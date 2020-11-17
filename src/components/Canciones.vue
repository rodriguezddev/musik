<template>
<div class="portadaDos">
    <div class="buscador">
        <input type="text" placeholder="Buscar">
        <span class="iconify lupa" data-icon="foundation:magnifying-glass" data-inline="false"></span>
    </div>
    <div class="clasificar">
        <P class="active">Canciones</P>
        <P>Albunes</P>
        <P>Artistas</P>
    </div>
    <div class="margin">
        <p class="titulo">Lo mas nuevo</p>
        <Carrusel />
    </div>
    <div class="margin">
        <p class="titulo">Lo mas buscado</p>
        <MasBuscado />
    </div>

</div>
</template>

<script>
import Carrusel from '@/components/Carrusel.vue'
import MasBuscado from '@/components/MasBuscado.vue'
export default {
    name: 'Canciones',
    components: {
        Carrusel,
        MasBuscado
    }
}
</script>

<style>
.portadaDos {
    background-color: rgb(0 0 0 / 90%);
    backdrop-filter: blur(5px);
    padding-bottom: 5rem;
}

.buscador {
    display: flex;
    padding: 1rem;
    align-items: center;
}

.buscador input {
    width: 100%;
    background-color: #2a2b2bb3;
    border: none;
    border-radius: 15px;
    padding: 7px 20px;
    outline: none;
    color: #fff
}

.lupa {
    font-size: 30px;
    margin: 0 1rem;
    color: #fff;
}

.titulo {
    font-size: 22px;
    font-family: 'GalanoGrotesque';
    letter-spacing: 0.1rem;
    text-align: start;
}

.margin {
    color: #fff;
    margin: 0 1rem;
}

.clasificar {
    display: flex;
    padding: 0 1rem;
    justify-content: center;
    margin-bottom: 1rem;
}

.clasificar p {
    font-family: 'HelveticaNeue';
    margin: 0;
    padding: 0 1rem;
    letter-spacing: 0.1rem;
    cursor: pointer;
}

.active {
    border-bottom: chocolate 1px solid;
}
</style>
