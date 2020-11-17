<template>
<div>
    <div v-for="(item,index) in canciones" :key="index">
        <router-link to="/Reproducir">
            <div class="shadow-lg contenedorCancion" @click="capturar(item)">
                <img :src="item.img" alt="">
                <div class="contInfo">
                    <div>
                        <p>{{item.name}}</p>
                        <p>{{item.artist}} - {{item.album}}</p>
                    </div>
                    <p class="duration">{{item.duration}}</p>
                </div>
            </div>
            
        </router-link>
    </div>
</div>
</template>

<script>
export default {

    data() {
        return {
            canciones: [{
                    name: 'Lover',
                    artist: 'Taylor Swift',
                    duration: '3:40',
                    album: 'Lover',
                    img: require('@/assets/taylor.jpg'),
                    song: require('@/assets/audio/14 Call It What You Want.mp3')
                },
                {
                    name: 'Gris',
                    artist: 'Jbalvin',
                    duration: '3:40',
                    album: 'Colores',
                    img: require('@/assets/colores.jpg'),
                    song: require('@/assets/audio/14 Call It What You Want.mp3')
                },
                {
                    name: 'Adore you',
                    artist: 'Harry Style',
                    duration: '3:40',
                    album: 'Fine line',
                    img: require('@/assets/harry.jpg'),
                    song: require('@/assets/audio/14 Call It What You Want.mp3')
                },
                {
                    name: 'Adore you',
                    artist: 'Harry Style',
                    duration: '3:40',
                    album: 'Fine line',
                    img: require('@/assets/dua.jpg'),
                    song: require('@/assets/audio/14 Call It What You Want.mp3')
                },
            ]
        }
    },
    methods: {
        capturar(item) {
            this.$bus.$emit('item', item)
            console.log(item)
        }
    }
}
</script>

<style>
.contenedorCancion {
    display: flex;
    margin-bottom: 1rem;
    background-color: #1919199e;
    border-radius: 8px;
    cursor: pointer;
    color: #fff;
}

.contenedorCancion img {
    width: 80px;
    height: 80px;
    border-radius: 8px;
}

.contenedorCancion p {
    margin: 0;
}

.contInfo {
    width: 100%;
    margin: 0.2rem 1rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.duration {
    text-align: end;
    color: chocolate;
    margin-top: 1rem;

}
</style>
