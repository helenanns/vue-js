<template>
    <img :src="avatar" :alt="descricao" height="50" width="50">
    <MudarImagem @mudar-imagem="trocarImagem" />
</template>


<script>
    import MudarImagem from './MudarImagem.vue';

    export default{
        name: 'Picture',
        components: {
            MudarImagem
        },
        data(){
            return{
                avatar: '/img/avatar.png',
                descricao: 'Imagem avatar'
            }
        },
        methods:{
            trocarImagem(){
                this.avatar = '/img/avatar2.png'
            }
        }
    }
</script>