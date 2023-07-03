<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else="esta_trabalhando">Estou em busca de novas oportunidades.</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>Javascript</li>
            <li>PHP</li>
            <li>Python</li>
        </ul>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    </div>
</template>

<script>
    export default{
        name: 'Info',
        data(){
            return{
                email: 'helena.nunes@futurasistemas.com.br',
                esta_trabalhando: false,
                mostrar_email: true
            }
        }
    }
</script>


