<script setup>
const props = defineProps(['operacao', 'a', 'b'])
</script>

<template>
<div class="container mt-5">
<div class="row">
  <div class="col md-5">
    <input @keyup="props.a" required type="number" placeholder="Número 1" class="form-control">
  </div>
  <div class="col md-2">
    <select @change="props.operacao" class="form-control">
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="*">*</option>
      <option value="/">/</option>
    </select>
  </div>
  <div class="col md-5">
    <input @keyup="props.b" required type="number" placeholder="Número 2" class="form-control">
  </div>
</div>
</div>
</template>