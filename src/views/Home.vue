<template>
<div class="home">
    <HelloWorld />
</div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
    name: 'Home',
    components: {
        HelloWorld
    }
}
</script>

<style>
.home {
    height: 100vh;
    background-image: url(../assets/vela.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;
}
</style>
