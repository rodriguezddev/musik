<template>
<div>
    <div class="portada">
        <div class="centro">
            <h1 class="name">Musik</h1>
            <p class="subname">Tu reproductor de musica favorito</p>
            <router-link to="/about"><span class="iconify play" data-icon="fa-solid:play" data-inline="false"></span></router-link>
            <p class="start">Empezar</p>
        </div>
    </div>
</div>
</template>

<script>
export default {


}
</script>

<style>
.portada {
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.76);
    backdrop-filter: blur(5px);
}

.centro {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
}

.name {
    color: #fff;
    font-size: 5.5rem;
    font-family: GalanoGrotesque;
    margin: 0;
    letter-spacing: 0.2rem;

}

.subname {
    color: #fff;
    font-size: 1rem;
    font-family: HelveticaNeue;
    letter-spacing: 0.2rem;
}

.play {
    color: #fff;
    font-size: 6rem;
    text-shadow: 4px 6px 9px rgba(130, 130, 130, 0.84);
    cursor: pointer;
}

.start {
    color: #fff;
    font-size: 1.3rem;
    margin-top: 2rem;
    font-family: HelveticaNeue;
    letter-spacing: 0.2rem;
}

.circulo {
    width: 30px;
    height: 30px;
    border-radius: 100px;
    background-color: #fff;
}
</style>
