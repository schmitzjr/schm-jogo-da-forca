<template>

    <div class="palavra">

        <div class="palavra-letras">

            <div v-for="(letra, key) in palavra" :key="key" class="palavra-letra">
                {{verificarLetra(letra) || etapa === 'enforcado' ? letra : ''}}
            </div>
            
        </div>

        <div class="palavra-dica">

            {{dica}}

        </div>

    </div>

</template>

<script>

export default {
    name: 'PalavraComp',
    props: {
        palavra: String,
        dica: String,
        etapa: String,
        verificarLetra: Function
    },
    components:{
        
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

.palavra{
    text-transform: uppercase;
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
}

.palavra-letra{
    margin: 0px 5px;
    height: 30px;
    width: 30px;
    border-bottom: 1px solid var(--color-text-light);
    display: flex;
    justify-content: center;
    align-items: center;
}

.palavra-letras{
    display: flex;
    margin-bottom: 20px;
}
    
</style>