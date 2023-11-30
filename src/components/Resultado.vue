<script setup>
    const props = defineProps(['a', 'b', 'result'])
</script>

<template>
    <span v-if="props.a && props.b !=''"><h2>Resultado: {{ props.result }}</h2></span>
    <span v-else-if="props.a || props.b ===''"><h2>Digite os números</h2></span>
</template>