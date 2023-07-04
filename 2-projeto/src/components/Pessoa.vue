<template>
    <h2>Descrição da pessoa: {{ nome }}</h2>
    <Info :email="email" :esta_trabalhando=false /> 
    <Form />
</template>

<script>
import Info from './Info.vue'
import Form from './Form.vue'
export default{
    name: 'Pessoa',
    components:{
        Info,
        Form
    },
    data(){
        return{
            nome: 'Helena',
            email: 'helena.nunes@futurasistemas.com.br'
        }
    }
}
</script>

