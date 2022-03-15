<template>

    <div class="forca">
        <img :src="`https://raw.githubusercontent.com/schmitzjr/schm-jogo-da-forca/master/public/images/${erros}.svg`">
    </div>

</template>

<script>

export default {
    name: 'ForcaComp',
    props: {
       erros: Number
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

.forca img{
    height: 100px;
}
    
</style>