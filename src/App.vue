<template>
  <div id="app">
    
    <Header 
    :contacts="contacts"/>

    <Main
    :contacts="contacts"/>

    <Footer 
    :contacts="contacts"/>

  </div>
</template>

<script>
import Header from './components/Header';
import Main from './components/Main';
import Footer from './components/Footer';

export default {
  name: 'App',
  data: function() {
    return {
      contacts: {
        openingTimes: "Mon - Sat - 9:00 - 18:00",
        phone: "+1 (305) 1234-5678" ,
        contactMail: "hello@example.com",
        address: "Main Avenue, 987"
      }
    }
  },
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import './style/general.scss';


</style>
