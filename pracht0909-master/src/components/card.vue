<script setup type="ts">
import bath from "./icones/bath.vue";
import heart from "./icones/heart.vue";

defineProps({
  nom: String,
  sousnom: String,
  permonth: String,
  prix: Number,
  favori: Boolean,
  image: String, // les images sont simplement l'URL absolue (depuis la racine, débute par '/' )
  nbrSDB: Number,
});



</script>

<template>
  <figure>

    <img class="w-full h-48 object-cover" src="src\assets\pexels-binyamin-mellish-106399 1.png">
    <figcaption class="relative flex flex-col border-2 border-t-0 border-indigo-100">

      <heart class="{ 'fill-red-300': favori }" />

      <div class="flex items-center">

        <div class="flex-grow-0 flex-shrink-0 text-2xl font-bold text-indigo-500">${{ prix }}2700</div>
        <div class="flex-grow-0 flex-shrink-0  text-gray-500">{{ permonth }}/month</div>

      </div>

      <h3 class="text-2xl text-gray-900">{{ nom }} Beverly Springfield</h3>
      <h5 class="text-gray-500 ">{{sousnom}} 2821 Lake Sevilla, Palm Harbor, TX</h5>
      <hr class="border-indigo-100 border-t-2 my-4" />

      <div>
        <bath class="inline-block pr-1" />{{ nbrSDB }} Bathrooms
      </div>
    </figcaption>
  </figure>
</template>