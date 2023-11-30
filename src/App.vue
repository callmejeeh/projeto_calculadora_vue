<script setup>
import {reactive} from 'vue';
import Calculadora from './components/Calculadora.vue'
import Resultado from './components/Resultado.vue'


const estado = reactive ({
  operation: '+',
  a: '',
  b: '',


})

const resultado = ()=> {
  const {operation} = estado
    switch(operation) {
      case'-':
      return parseFloat(estado.a) - parseFloat(estado.b)
      case'*':
      return parseFloat(estado.a) * parseFloat(estado.b)
      case'/':
      return parseFloat(estado.a) / parseFloat(estado.b)
      default:
      return parseFloat(estado.a) + parseFloat(estado.b)
    }
}


</script>

<template>
    <div class="container">
      <Calculadora :operacao="evento=> estado.operation = evento.target.value" :a="evento=> estado.a = evento.target.value" :b="evento=> estado.b=evento.target.value" />
      <Resultado :a="estado.a" :b="estado.b" :result="resultado()"/>
    </div>
  </template>

<style scoped>

</style>
