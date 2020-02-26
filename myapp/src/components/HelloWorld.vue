<template>

    

    <v-carousel>
        <v-carousel-item
                v-for="(item,i) in items"
                :key="i"
                :src="item.src"
                reverse-transition="fade-transition"
                transition="fade-transition"
        ></v-carousel-item>
    </v-carousel>


</template>

<script>
    export default {
        data () {
            return {
                items: [
                    {
                        src: 'https://i.imgur.com/mRV9kjI.png',
                    },
                    {
                        src: 'https://wallpapercave.com/wp/wp4036432.jpg',
                    },
                    {
                        src: 'https://wallpapercave.com/wp/wp4036437.png',
                    },
                    {
                        src: 'https://images7.alphacoders.com/784/thumb-1920-784913.png',
                    },
                ],
            }
        },
    }
</script>