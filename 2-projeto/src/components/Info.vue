<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else="esta_trabalhando">Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>Javascript</li>
            <li>PHP</li>
            <li>Python</li>
        </ul>
        <div>
            <button @click="showEmail">Mostrar e-mail</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p class="teste">Para acessar meu portfólio <a v-bind:href="url_portfolio" target="_blank">clique aqui</a></p>
        <Picture />
    </div>
</template>

<script>
    import Picture from './Picture.vue';
    export default{
        name: 'Info',
        components: {
            Picture
        },
        data(){
            return{
                email: 'helena.nunes@futurasistemas.com.br',
                esta_trabalhando: false,
                mostrar_email: false,
                url_portfolio: 'https://google.com'
            }
        },
        methods:{
            showEmail(){
                this.mostrar_email = !this.mostrar_email;
            }
        }
    }
</script>

<style>
.paragrafo-pai{
    color: red;
}
</style>