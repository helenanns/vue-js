<template>
    <img :src="avatar" alt="" height="50" width="50">
</template>


<script>
    export default{
        name: 'Picture',
        data(){
            return{
                avatar: '/img/avatar.png'
            }
        }
    }
</script>