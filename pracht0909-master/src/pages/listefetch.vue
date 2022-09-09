<template>
    <h1 class="font-bold text-xl mt-8 mb-8">Page Liste</h1>
    <div v-for="maisons in maisons" :key="maisons.nom">
        <card class="w-1/2" v-bind="maisons" />
    </div>
</template>

<script setup lang="ts">
import card from "../components/card.vue";

const res = await fetch("maisons.json");
const maisons = await res.json();
</script>