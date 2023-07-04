<template>
    <header>
        <router-link to="/">
            <img alt="Vue logo" class="logo" src="../../public/img/logo.png" width="125" height="125" />
        </router-link>

        <div class="wrapper">
            <HelloWorld msg="You did it!" />
            <nav>
                <RouterLink to="/">Home</RouterLink>
                <RouterLink to="/pedidos">Pedidos</RouterLink>
            </nav>
        </div>
    </header>
</template>
<script>
export default{
    name: 'Navbar'
}
</script>