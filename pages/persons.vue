<template>
    <v-container>
        <PersonInformation :name="nameData" :age="ageData"/>
    </v-container>
</template>

<script lang="ts">
export default {
    name: "Persons",

    data: () => ({
        nameData: "Marcos Antonio Perez Villegas",
        ageData: 22
    })
}
</script>

<i18n lang="json">
{
    "es": {},
    "en": {}
}
</i18n>