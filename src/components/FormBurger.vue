<template>
    <v-container>
        <p text_center>component_mensagem</p>
        <v-row justify="center" class="my-10">
            <v-col cols="12" sm="10" md="8" lg="5">
                <v-card ref="form">
                    <v-card-text style="background-color: white" class="pt-6">
                        <!--NOME-->
                        <v-text-field ref="name" outlined dense v-model="name"
                            :rules="[() => !!name || 'Necessário preencher este campo']" :error-messages="errorMessages"
                            label="Nome" placeholder="John Doe" required>
                        </v-text-field>

                        <!--PAO-->
                        <v-autocomplete outlined dense ref="country" v-model="country"
                            :rules="[() => !!country || 'Escolha uma opção']" :items="countries" label="Escolha o pão"
                            placeholder="Select..." required></v-autocomplete>


                        <!--CARNE-->
                        <v-autocomplete outlined dense ref="country" v-model="country"
                            :rules="[() => !!country || 'Escolha uma opção']" :items="countries"
                            label="Escolha a carde do seu Burger" placeholder="Select..." required></v-autocomplete>

                        <!--OPCIONAIS-->
                        <v-row class="pa-4">
                            <v-checkbox class="mr-4" v-for="(opcional, index) in opcionais" :key="index"
                                :v-model="opcional.checked" :label="opcional.tipo"></v-checkbox>
                            <!--OPCIONAIS-->
                        </v-row>

                        <v-row class="pa-4">
                            <v-select :items="opcionais" item-text="tipo"
                                item-value="value" label="Selecionar opcionais" outlined attach multiple chips>
                            </v-select>
                        </v-row>

                    </v-card-text>
                    <v-card-actions style="background-color: white" class="pa-4">
                        <v-spacer></v-spacer>
                        <v-btn text> Cancel </v-btn>
                        <v-btn color="error" @click="submit"> Fazer pedido </v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script lang="ts">
export default {
    name: "FormBurger",
    data: () => ({

        value: ['foo', 'bar', 'fizz', 'buzz'],
        countries: [
            "Afghanistan",
            "Albania",
            "Algeria",
            "Andorra",
            "Angola",
            "Anguilla",
            "Antigua &amp; Barbuda",
            "Argentina",
            "Armenia",
            "Aruba",
        ],

        opcionais: [
            {
                "id": 1,
                "tipo": "Bacon",
                "value": "bacon"
            },
            {
                "id": 2,
                "tipo": "Cheddar",
                "value": "cheddar"
            },
            {
                "id": 3,
                "tipo": "Salame",
                "value": "salame"

            },
            {
                "id": 4,
                "tipo": "Tomate",
                "value": "tomate"
            },
            {
                "id": 4,
                "tipo": "Cebola roxa",
                "value": "cebola-roxa"
            },
            {
                "id": 4,
                "tipo": "Pepino",
                "value": "pepino"
            }
        ],
        errorMessages: "",
        name: null,
        country: null,
        formHasErrors: false,
    }),

    computed: {
    },
    watch: {
    },
    methods: {
    },
};
</script>

<style lang="scss">
</style>
