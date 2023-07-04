<template>
    <div>
        <p>{{ email }}</p>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else="esta_trabalhando">Estou em busca de novas oportunidades!</p>

        <p>Utilizo as seguintes tecnologias para back-end:</p>
        <ul>
            <li v-for="(technology, index) in backend_technologies" v-bind:key="index">
                {{technology}}
            </li>
        </ul>

        <p>Utilizo as seguintes tecnologias para front-end:</p>
        <ul>
            <li v-for="technology in frontend_technologies" :key="technology.id">
                {{ technology.language }}
            </li>
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
        props: {
            email: String,
            esta_trabalhando: Boolean,
        },
        data(){
            return{
                mostrar_email: false,
                url_portfolio: 'https://google.com',
                backend_technologies: ['Javascript', 'PHP', 'Python'],
                frontend_technologies: [
                    {id: 1, language: 'HTML'},
                    {id: 3, language: 'CSS'},
                    {id: 4, language: 'Vue'},
                ]
            }
        },
        methods:{
            showEmail(){
                this.mostrar_email = !this.mostrar_email;
            }
        }
    }
</script>