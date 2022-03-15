<template>

    <div class="jogo">

        <Forca
            :erros="erros"
            :palavra="palavra"
            :dica="dica"
        />

        <Palavra
            :palavra="palavra"
            :dica="dica"
            :verificarLetra="verificarLetra"
            :etapa="etapa"
        />

        <Teclado
            v-if="etapa === 'jogo'"
            :letras="letras"
            :verificarLetra="verificarLetra"
            :jogar="jogar"
        />

        <Final
            v-if="etapa != 'jogo'"
            :etapa="etapa"
            :texto="etapa ==='ganhador' ? 'Parabéns ;)' : 'Errou! :('"
            :jogarNovamente="jogarNovamente"
        />

    </div>

</template>

<script>

import Forca from './Forca';
import Palavra from './Palavra';
import Teclado from './Teclado';
import Final from './Final';

export default {
    name: 'JogoComp',
    props: {
       erros: Number,
       palavra: String,
       dica: String,
       etapa: String,
       verificarLetra: Function,
       letras: Array,
       jogar: Function,
       jogarNovamente: Function
    },
    components:{
        Forca,
        Palavra,
        Teclado,
        Final
    },
    data() {
        return {
           
        }
    },
    methods: {
        
    },
}

</script>

<style>

.jogo{
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}
    
</style>