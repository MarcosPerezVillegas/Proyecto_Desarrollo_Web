<template>
    <v-container>
        <v-card>
            <v-card-tittle>Marcos Antonio Perez Villegas</v-card-tittle>
            <v-card-text>
                Ingeniero en Electrónica y Computación
                <br>
            {{ counter }}
            <br>
            <br>
            {{ counterAndName }}
            <br>
            <br>
            {{ $t('help') }}
            </v-card-text>
            <v-card-actions>
                <v-spacer/>
                <v-btn @click="sumOneToCounter()">
                    Click Me!
                </v-btn>
            </v-card-actions>
        </v-card>
    </v-container>
  </template>
  
  <script lang="ts">

  export default {
    name: 'AboutMe',

    data(){
        return{
            counter: 1 
        }
    },  

    watch: {
        counter(){

        }
    },

    computed: {
        counterAndName(){
            return this.counter + "Marcos"
        }
    },

    beforeMount(){
        this.counter++
    },

    methods: {
        sumOneToCounter(){
            this.counter++
        }
    }
  }
  </script>
  
  <i18n lang="json">{
    "es": {
        "help": "Ayuda"
    },
    "en":{
        "help": "Help"
    }
  }
  </i18n>