<template>
  <div id="app">
    <TopMenu/>
    <Header/>
    <router-view/>
    <Footer/>
  </div>
</template>

<script>
import TopMenu from './components/TopMenu.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
export default {
  name: 'App',
  components: {
    TopMenu,
    Header,
    Footer
  }
}
</script>

<style>
</style>