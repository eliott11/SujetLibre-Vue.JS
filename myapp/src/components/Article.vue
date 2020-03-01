<template>
    <div>
    <!-- Article avec avatar et contenu -->
        <v-row class="align-content-center" justify="space-around">
            <v-avatar>
                <img src="https://cdn4.iconfinder.com/data/icons/superheroes/512/ironman-512.png" alt="Pathfinder">
            </v-avatar>
        </v-row>

        <div class="text-center">
           <ul>
               <li v-for ="item in items" v-bind:key="item">
                   {{ item }}
               </li>
           </ul>
        </div>

        <br><br>
    </div>
</template>

<script>
    export default {
        el: '#v-for-object',
        data () {
            return {
                items: {
                    title: 'Article 1',
                    author: 'Pathfinder',
                    date: '2016-04-10',
                    text: 'Hello, this is my first article'
                },
            }
        },
    }
</script>