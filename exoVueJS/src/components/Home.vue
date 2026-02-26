<template>
    <component :is="exercices[indexExo]" />

    <div class="container">
        <button @click="precedent" :disabled="indexExo === 0">
            Précédent
        </button>
        <span>Exercice {{ indexExo + 1 }}/{{ exercices.length }}</span>
        <button @click="suivant" :disabled="indexExo === exercices.length - 1">
            Suivant
        </button>
    </div>
</template>



<script setup>
import { ref } from 'vue'

import Exo1 from './Exo1.vue'
import Exo2 from './Exo2.vue'
import Exo3 from './Exo3.vue'
import Exo4 from './Exo4.vue'
import Exo5 from './Exo5.vue'
import Exo6 from './Exo6.vue'
import Exo7 from './Exo7.vue'
import Exo8 from './Exo8.vue'
import Exo9 from './Exo9.vue'
import Exo10 from './Exo10.vue'
import Exo11 from './Exo11.vue'
import Exo12 from './Exo12.vue'
import Exo13 from './Exo13.vue'
import Exo14 from './Exo14.vue'
import Exo15 from './Exo15.vue'
import Exo16 from './Exo16.vue'
import Exo17 from './Exo17.vue'
import Exo18 from './Exo18.vue'
import Exo19 from './Exo19.vue'
import Exo20 from './Exo20.vue'

const exercices = [
    Exo1, Exo2, Exo3, Exo4, Exo5,
    Exo6, Exo7, Exo8, Exo9, Exo10,
    Exo11, Exo12, Exo13, Exo14, Exo15,
    Exo16, Exo17, Exo18, Exo19, Exo20
]

const indexExo = ref(0)

const suivant = () => {
    if (indexExo.value < exercices.length - 1) {
        indexExo.value++
    }
}

const precedent = () => {
    if (indexExo.value > 0) {
        indexExo.value--
    }
}
</script>


<style>

.container {
    display: flex;
    justify-content: space-evenly;
    align-items: baseline;
    margin-top: 3rem;
}


</style>


