<template>
    <div class="calculadora">
        <resul />
        <botoes />
    </div>
</template>
<script>
import Botoes from './botoes.vue'
import resul from './resul.vue'
export default {
    name: `calculadora`,
    components: { resul, Botoes}
}
</script>
<style>
    .calculadora{
        background-color: black ;
        width: 250px;
        height: 500px;
    }
</style>