<template>
  <div id="app">
    
    <Header 
    :contacts="contacts"
    :navLinks="navLinks"/>

    <Main
    :contacts="contacts"/>

    <Footer 
    :contacts="contacts"
    :about="about"
    :services="services"
    :support="support" />

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
      },
      // header
      navLinks: [
        {
            name: "Home",
            url: "#home"
        },
        {
            name: "Services",
            url: "#services"
        },
        {
            name: "About",
            url: "#company"
        },
        {
            name: "Projects",
            url: "#projects"
        },
        {
            name: "Results",
            url: "#results"
        }
      ],
      // footer
      about: [
        {
          name: "The Company",
          url: "#company"
        },
        {
          name: "Institutional",
          url: "#projects"
        },
        {
          name: "Social & Events",
          url: "#projects"
        },
        {
          name: "Innovation",
          url: "#projects"
        },
        {
          name: "Environment",
          url: "#projects"
        },
        {
          name: "Technology",
          url: "#projects"
        }                
      ],
      services: [
        {
          name: "Audit & Assurance",
          url: "#services"
        },
        {
          name: "Financial Advisory",
          url: "#services"
        },
        {
          name: "Analytics and M&A",
          url: "#services"
        },
        {
          name: "Middle Marketing",
          url: "#services"
        },
        {
          name: "Legal Consulting",
          url: "#services"
        },
        {
          name: "Regiulatory Risk",
          url: "#services"
        }
      ],
      support: [
        {
          name: "Responsibility",
          url: ""
        },
        {
          name: "Terms of Use",
          url: ""
        },
        {
          name: "About Cookies",
          url: ""
        },
        {
          name: "Privacy Policy",
          url: ""
        },
        {
          name: "Accessibility",
          url: ""
        },
        {
          name: "Information",
          url: ""
        }
      ]
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
