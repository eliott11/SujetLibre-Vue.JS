<template>
    <div>
    <!-- Article animé avec avatar et contenu -->

        <v-expansion-panels>
            <v-expansion-panel
                    v-for="(item,i) in 1"
                    :key="i"
            >
                <div class="text--primary">
                    <v-hover>
                        <template v-slot="{ hover }">
                            <v-card :elevation="hover ? 24 : 6" class="mx-auto pa-6">
                                <div class="text-center">
                                      <v-expansion-panel-header>
                                          <v-row class="align-content-center">
                                                <v-avatar>
                                                  <img src="https://cdn4.iconfinder.com/data/icons/superheroes/512/ironman-512.png" alt="Iron Man">
                                              </v-avatar>
                                              (cliquez ici)
                                          </v-row>
                                      </v-expansion-panel-header>

                                      <v-expansion-panel-content>
                                          <ul>
                                             <li v-for ="item in items" v-bind:key="item">
                                                  {{ item }}
                                               </li>
                                           </ul>
                                       </v-expansion-panel-content>
                                </div>
                            </v-card>
                        </template>
                    </v-hover>
                    <div class="my-6"></div>
                </div><br><br>
            </v-expansion-panel>
        </v-expansion-panels><br><br>


    </div>
</template>

<script>
    export default {
        el: '#v-for-object',
        data () {
            return {
                items: {
                    author: 'Iron Man',
                    date: '29 février 2020',
                    title: 'Article 1',
                    text: 'Bonjour, Voici mon premier article sur le jeu vidéo Astroneer'
                },
            }
        },
    }
</script>