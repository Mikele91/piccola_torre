<template>
  <div class="">
  <Header/>
  <Main/>
  <Footer/>
  </div>
 
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header'
import Main from './components/Main'
import Footer from './components/Footer'


export default {
  name: 'App',
  components: {
    //HelloWorld,
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import "./assets/style/global.scss";
@import "./assets/style/globalParts/variables.scss";
#app {
  //max-width:$container_width;
  
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
