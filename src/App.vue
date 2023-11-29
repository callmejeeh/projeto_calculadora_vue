<script setup>
import {reactive} from 'vue';


const estado = reactive ({
  a: '',
  b: '',
  resultado: ''

})

function add(resultado){
  resultado = estado.a + estado.b;
  alert(resultado);
    } 

    function minus(resultado){
  resultado = estado.a - estado.b;
  alert(resultado);
    } 
    function times(resultado){
  resultado = estado.a * estado.b;
  alert(resultado);
    } 
    function divide(resultado){
  resultado = estado.a / estado.b;
  alert(resultado);
    } 


</script>

<template>
<div class="container mt-5">
<div class="row">
  <div class="col md-5">
    <input v-model.number="estado.a" placeholder="Número" class="form-control">
  </div>
  <div class="col md-2">
    <select class="form-control">
      <option value="selecionar">Selecione</option>
      <option @click="add" value="adicao">+</option>
      <option @click="minus" value="subtracao">-</option>
      <option @click="times" value="multiplicacao">*</option>
      <option @click="divide" value="divisao">/</option>
    </select>
  </div>
  <div class="col md-5">
    <input v-model.number="estado.b" class="form-control">
  </div>
</div>
<div class="col">

</div>
</div>
</template>

<style scoped>

</style>
