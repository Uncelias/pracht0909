<template>
    <h1 class="font-bold text-xl mt-8 mb-8">Page Liste</h1>
    <div v-for="maisons in maisons" :key="maisons.nom">
        <card class="w-1/2" v-bind="maisons" />
    </div>
</template>

<script setup lang="ts">
import Card from "../components/card.vue";

const maisons = [{ nom: "N°1", }, { nom: "N°4" }, { nom: "N°3", }, { nom: "N°4", },]
</script>