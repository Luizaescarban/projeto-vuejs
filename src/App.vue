<script setup>
import {ref, onMounted} from "vue"
const contador = ref(0);

function incrementar() {
  contador.value ++;
}
function decrementar(){
  if (contador.value > 0) {
    contador.value --;
  }
}

function reiniciar (){
  contador.value = 0;
}
onMounted (() => {
  console.log(`O valor inicial do contador é ${contador.value}`)
})

</script>

<template>
  <button @click="incrementar">+</button>
  <button @click="decrementar">-</button>
  <button @click="reiniciar">Reiniciar</button>
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
