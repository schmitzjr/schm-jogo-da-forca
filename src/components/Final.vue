<template>

    <div class="final">
        
        <div :class="`final-texto-${etapa}`">
            {{texto}}
        </div>

        <button
            v-on:click="jogarNovamente()" 
            class="final-botao">Jogar novamente
        </button> 

    </div>

</template>

<script>

export default {
    name: 'FinalComp',
    props:{
        etapa: String,
        texto: String,
        jogarNovamente: Function
    }
}

</script>

<style>

.final-texto{
    margin: 20px 0px;
    font-size: 24px;
    font-weight: bold;
}

.final-texto-enforcado{
    margin-top: 30px;
    margin-bottom: 10px;
    color: var(--color-text-error);
}

.final-texto-ganhador{
    margin-top: 30px;
    margin-bottom: 10px;
    color: var(--color-text-success);
}

</style>



