<template>
  <div class="container">
    <calculadora />
  </div>
</template>
<script>
import calculadora from "./components/calculadora.vue"

export default {
  components: { calculadora },
  
}
</script>
<style>
.container{
  display: flex;
  height: 100vh;
  align-items: center;
  justify-content: center;
}
</style>