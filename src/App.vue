<script>
import Header from './components/Header.vue';
import Main from './components/main.vue';
import Footer from './components/footer.vue';


export default {
  name : 'App',
  components : { Header,
  Main,
  Footer 
}
}
</script>

<template>
  <Header/>
  <Main/>
  <Footer/>
</template>

<style lang="scss">
@use './scss/main.scss'
</style>
