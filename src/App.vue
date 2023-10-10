<script>
import Header from './components/header.vue';
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

  <h1>App</h1>
</template>

<style lang="scss">
@use './scss/main.scss'
</style>
