<template>
<div>
    <audio :src="track.song" controls></audio>
    <img :src="track.img" alt="">
</div>
</template>

<script>
export default {
    data() {
        return {
            track: {}
        }
    },
    methods:{
        enviar(){
                this.$bus.$on('item', (item) => {
                this.track = item
                console.log(this.track)
            })
        }
    },
    created() {
       this.enviar()
    }
}
</script>
