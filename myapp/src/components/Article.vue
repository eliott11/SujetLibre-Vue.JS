<template>
    <div>
    <!-- Article avec avatar et contenu -->

        <div class="text--primary">
            <!-- Using the elevation prop -->
            <v-hover>
                <template v-slot="{ hover }">
                    <v-card :elevation="hover ? 24 : 6" class="mx-auto pa-6">
                        <div class="text-center">
                            <v-row class="align-content-center" justify="space-around">
                                <v-avatar>
                                    <img src="https://cdn4.iconfinder.com/data/icons/superheroes/512/ironman-512.png" alt="Pathfinder">
                                </v-avatar>
                            </v-row>
                            <ul>
                                <li v-for ="item in items" v-bind:key="item">
                                    {{ item }}
                                </li>
                            </ul>
                        </div>
                    </v-card>
                </template>
            </v-hover>
            <div class="my-6"></div>
        </div><br><br>
    </div>
</template>

<script>
    export default {
        el: '#v-for-object',
        data () {
            return {
                items: {
                    author: 'Pathfinder',
                    date: '29 février 2020',
                    title: 'Article 1',
                    text: 'Hello, this is my first article'
                },
            }
        },
    }
</script>