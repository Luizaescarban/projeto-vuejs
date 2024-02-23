<script setup>
import {ref, onMounted} from "vue"
const contador = ref(0)

function decrementar(){
  contador.value--
}
onMounted (() => {
  console.log(`O valor inicial do contador é ${contador.value}`)
})
function 
</script>

<template>
  <button @click="contador++">+</button>
  <button @click="decrementar">-</button>
  <p>Valor do contador: {{ contador }}</p>
</template>

<style scoped>

button{
  font-weight: bold;
  background-color: blue;
  color: white;
  border: 0;
}

</style>
