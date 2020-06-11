<template>
  <div>
    <Header/>
    <Intro/>
    <CoronaDeaths/>
    <CoronaNews/>
    <End/>
    <Footer/>
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

import Header from './components/Header.vue'
import Intro from './components/Intro'
import CoronaDeaths from './components/CoronaDeaths'
import CoronaNews from './components/CornaNews'
import End from './components/End'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Header,
    Intro,
    CoronaDeaths,
    CoronaNews,
    End,
    Footer
  },
}
</script>


<style>
#app {
  font: sans-serif, Helvetica, Arial;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 0px
}

::-webkit-scrollbar {
  width: 15px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1; 
}
 
::-webkit-scrollbar-thumb {
  background: #8BD8BD; 
}

::-webkit-scrollbar-thumb:hover {
  background: #243665; 
}

</style>
