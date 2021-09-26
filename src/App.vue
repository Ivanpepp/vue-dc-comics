<template>
  <div id="app">
    
    <Header />
    <Main />
    <Footer />

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
/* RESET */
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.my-view{
   width: 1300px;
  margin: 0 auto;
}
#app {
 font-family: 'Gemunu Libre';
 height: 100vh;
}
</style>
