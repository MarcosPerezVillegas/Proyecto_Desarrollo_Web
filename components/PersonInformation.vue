<template>
    <v-card>
        <v-cardt-tittle>
            {{ nameWithCaption }}
        </v-cardt-tittle>
        <v-card-text>
            {{ ageWithCaption }}        
        </v-card-text>
    </v-card>
</template>

<script lang="ts">
export default {
    name: "PersonInformation",

    props: {
        name: {
            type: String,
            required: false,
            default: "Marcos",
        },

        age: {
            type: Number,
            required: true,
            default: 22
        },
    },

    computed: {
        nameWithCaption() {
            return this.$t('name_Caption')+ this.name
        },

        ageWithCaption() {
            return this.$t('age_Caption')+this.age
        }
    }

}
</script>

<i18n lang="json">
{
    "es": {
        "name_Caption": "Nombre: ",
        "age_Caption": "Edad: "
    },
    "en": {
        "name_Caption": "Name: ",
        "age_Caption": "Age: "
    }
}
</i18n>