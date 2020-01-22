<template>
  <div id="app">
    <UserD></UserD>
    <page-t></page-t>
    <nav-cont></nav-cont>    
    <main-cont></main-cont>
  </div>
</template>

<script>
import UserD from './components/UserDetail.vue'
import PageT from './components/PageTitle.vue'
import NavCont from './components/NavContent.vue'
import MainCont from './components/MainContent.vue'

export default {
  name: 'app',
  components: {
    UserD, PageT, NavCont, MainCont
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: inline;
}
body{
  height: 100vh;
  width: 100%;
}

</style>
