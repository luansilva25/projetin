<template>
    <div class="calculadora">
        <botoes />
    </div>
</template>
<script>
import Botoes from './botoes.vue'
export default {
    name: `calculadora`,
    components: {Botoes}
}
</script>
<style>
    .calculadora{
        background-color: black ;
        width: 300px;
        height: 600px;
        padding: 20px;

    }

</style>