<template>
  <Navbar :logo="logo_src" :alt="app_name" />
  <RouterView />
  <Footer />
</template>



<script>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';

export default{
  components: {
    Navbar,
    Footer
  },
  data(){
    return{
      logo_src: '/img/logo.png',
      app_name: 'Hamburger'
    }
  }
}

</script>

