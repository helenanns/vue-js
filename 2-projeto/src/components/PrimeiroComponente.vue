<template>
    <h1>Oi!</h1>
    <MultiplosEventos /> 
    <Reutilizacao /> 
    <Reutilizacao /> 
</template>


<script>
    import MultiplosEventos from './MultiplosEventos.vue';
    import Reutilizacao from './Reutilizacao.vue';

    export default{
        name: 'PrimeiroComponente',
        components: { MultiplosEventos, Reutilizacao }
    }
</script>