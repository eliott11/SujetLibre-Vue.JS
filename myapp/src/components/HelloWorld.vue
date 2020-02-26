<template>
    <div>
    <v-carousel>
        <v-carousel-item
                v-for="(item,i) in items"
                :key="i"
                :src="item.src"
                reverse-transition="fade-transition"
                transition="fade-transition"
                style="height: auto"
        ></v-carousel-item>
    </v-carousel> <br><br>
    <h1 class="text-center font-weight-black font-size:70px">Astroneer</h1> <br><br><br><br><br>
    <h2 class="text-center">Qu'est-ce que c'est ?</h2><br><br>
    <h3 class="text-center">Astroneer est un jeu vidéo de type bac à sable sorti sur PC <br>
        le 16 décembre 2016 en pré-alpha sur Steam, et créé par System Era Softworks. <br>
        Une version finalisée est distribuée le 6 février 2019.</h3><br><br>
    </div>

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