<template>
  <div id="app">
    <Header />
    <Jumbotron />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header';
import Jumbotron from './components/Jumbotron';
import Main from './components/Main';
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Main,
    Footer
  }
}
</script>

<style lang="scss">

</style>
