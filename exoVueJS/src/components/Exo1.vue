<template>

<h1>Exercice 1 — Message dynamique</h1>
<button @click="message = !message">Changer le message</button>
<p v-if="message">Hello world !!!</p>
<p v-else>Bonjour le monde !!!</p>

</template>



<script setup>
import { ref } from 'vue'

const message = ref(true)


</script>


<style>

button {
  background-color: orangered;
  margin-top: 1rem;
  margin-bottom: 1.5rem;
}


</style>