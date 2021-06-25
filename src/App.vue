<template>
  <div id="app">
    <Header :item='menuVoices'/>
    <Main />
    <Footer :item='usefulInfo'/>
  </div>
</template>

<script>
import Header from './components/Header';
import Main from './components/Main';
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data() {
    return {
      menuVoices: ["Find Your New Barber","Services","Products","Reviews","Blog Posts"],
      usefulInfo: {
        name: "Avada Barbers",
        address: "123 New York Street",
        city: "New York City",
        email: "info@yourwebsite.com",
        number: "+1 (555) 555-1212"
      }
    }
  }
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap.scss';
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
</style>