<template>
    <div>

        <v-row justify="center">

            <v-dialog v-model="dialog" persistent max-width="600px">
                <template v-slot:activator="{ on }">
                    <v-btn color="primary" dark v-on="on">Intéressé ?</v-btn>
                </template>

                <v-card>
                    <v-card-title>
                        <span class="headline">Vos informations</span>
                    </v-card-title>
                    <v-card-text>
                        <v-container>
                            <v-row>
                                <v-col cols="12" sm="6" md="4">
                                    <v-text-field label="Nom*" required></v-text-field>
                                </v-col>

                                <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                            label="Prénom*"
                                            persistent-hint
                                            required
                                    ></v-text-field>
                                </v-col>

                                <v-col cols="12">
                                    <v-text-field label="Email*" required></v-text-field>
                                </v-col>

                                <v-col cols="12" sm="6">
                                    <v-select
                                            :items="['0-17', '18-29', '30-54', '54+']"
                                            label="Age*"
                                            required
                                    ></v-select>
                                </v-col>

                                <v-col cols="12" sm="6">
                                    <v-autocomplete
                                            :items="['Prix', 'Date', 'Evenements', 'Infos du jeu']"
                                            label="Motif*"
                                            required
                                            multiple
                                    ></v-autocomplete>
                                </v-col>
                            </v-row>
                        </v-container>
                            <small>*Obligatoire</small>
                    </v-card-text>

                    <v-card-actions>
                        <v-spacer></v-spacer>
                        <v-btn color="blue darken-1" text @click="dialog = false">Fermer</v-btn>
                        <v-btn color="blue darken-1" text onclick='window.location.reload(false)'>Envoyer</v-btn>
                    </v-card-actions>
                </v-card>
            </v-dialog>
        </v-row><br><br>

        <v-footer padless>
            <v-col
                    class="text-center"
                    cols="14"
            >
                {{ new Date().getFullYear() }} — <strong>ASTRONEER</strong>
            </v-col>
        </v-footer>

</div>
</template>


<script>
    export default {
        data: () => ({
            dialog: false,
        }),
    }
</script>