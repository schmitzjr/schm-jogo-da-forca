<template >
    <div class="teclado">

      <button
        class="teclado-botao" 
        v-for="(letra, key) in alfabeto" 
        :key="key"
        :disabled="verificarletra(letra)"
        v-on:click="jogar(letra)"
        
      >{{letra}}</button> 
        
    </div>
</template>

<script>
export default {
    name: "TecladoComp",
    data() {
      return {
        alfabeto:['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
      }
    },
    props:{
      letras: Array,
      verificarletra: Function,
      jogar: Function
    }
}
</script>

<style>

.teclado{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  max-width: 85%;
  margin-top: 20px;
}

.teclado-botao{
  margin: 5px;
  text-transform: uppercase;
}
</style>