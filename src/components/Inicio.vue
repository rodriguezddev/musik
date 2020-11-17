<template>
<div class="inicio">
    <router-link to="/"><span class="iconify arrow" data-icon="heroicons-solid:arrow-narrow-left" data-inline="false"></span></router-link>
    <div id="inicio" class="centro">
        <h1>Iniciar</h1>
        <div class="container">
            <div class="inputs">
                <span class="iconify acceder" data-icon="ant-design:user-outlined" data-inline="false"></span>
                <input type="text" placeholder="Usuario" name="" id="">
            </div>

            <div class="inputs">
                <span class="iconify acceder" data-icon="bx:bx-lock" data-inline="false"></span>
                <input type="password" placeholder="Contraseña" name="" id="">
            </div>
            <button type="submit" class="btn button shadow-lg">Entrar</button>
            <div class="options">
                <p @click="formUno()">Crear una cuenta</p>
                <p>Olvide mi contraseña</p>
            </div>
        </div>
    </div>
    <div id="registro" style="display:none" class="centro">
        <h1>Registrarse</h1>
        <div class="container">
            <div class="inputs">
                <span class="iconify acceder" data-icon="ant-design:user-outlined" data-inline="false"></span>
                <input type="text" placeholder="Usuario" name="" id="">
            </div>
            <div class="inputs">
                <span class="iconify acceder" data-icon="ic:outline-email" data-inline="false"></span>
                <input type="email" placeholder="Correo" name="" id="">
            </div>
            <div class="inputs">
                <span class="iconify acceder" data-icon="bx:bx-lock" data-inline="false"></span>
                <input type="password" placeholder="Contraseña" name="" id="">
            </div>
            <button type="submit" class="btn button shadow-lg">Entrar</button>
            <div class="options">
                <p @click="formDos()">Ya tengo un cuenta</p>
                <p>Olvide mi contraseña</p>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {

        }
    },
    methods: {
        formUno() {
            document.getElementById('inicio').style.display = 'none'
            document.getElementById('registro').style.display = 'flex'
        },
        formDos() {
            document.getElementById('inicio').style.display = 'flex'
            document.getElementById('registro').style.display = 'none'
        }
    }
}
</script>

<style>
.inicio {
    height: 100vh;
    background-color: rgb(0 0 0 / 90%);
    backdrop-filter: blur(5px);
    color: #fff;
}

.centro {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
}

.centro h1 {
    font-family: GalanoGrotesque
}

.inputs {
    display: flex;
    width: 100%;
    justify-content: space-around;
    margin: 2rem 0;
}

.inputs input {
    width: 70%;
    background: transparent;
    border: 0;
    border-bottom: 1px solid;
    outline: none;
    color: #fff;
    padding-left: 2.5rem;
}

.container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 30rem;
}

.acceder {
    margin-right: -10rem;
    font-size: 35px;
    margin-bottom: 10px;
}

.button {
    width: 70%;
    padding: 0.5rem 0;
    border-radius: 15px;
    color: #fff;
    background-image: linear-gradient(to right top, #891414, #760031, #540b40, #2c1540, #021432);
}

.options {
    font-family: HelveticaNeue;
    display: flex;
    width: 100%;
    justify-content: space-around;
    letter-spacing: 0.6px;
    margin-top: 1rem;
}

.options p {
    cursor: pointer;
}

.arrow {
    font-size: 30px;
    position: absolute;
    left: 2rem;
    margin-top: 2rem;
}

.router-link-active {
    color: #fff
}
</style>
