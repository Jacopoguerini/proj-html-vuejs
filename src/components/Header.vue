<template>
    <header>
        <div class="info-bar">
            <div class="container flex-spbt-centre">
                <!-- opening times -->
                <div class="nav-opening-times">
                    <i class="fas fa-clock"></i>
                    <span>
                    Open Hours: {{ openingTimes }}
                    </span>
                </div>
                <!-- /opening times -->

                <!-- contacts -->
                <ul class="nav-contacts list-inline">
                    <!-- phone number -->
                    <li>
                        <i class="fas fa-phone-alt"></i>
                        <span>{{ phone }}</span>
                    </li>
                    <!-- /phone number -->

                    <!-- mail -->
                    <li>
                        <i class="fas fa-envelope"></i>
                        <span>{{ contactMail }}</span>
                    </li>
                    <!-- /mail -->

                    <!-- social contacts -->
                    <li>
                        <a href="#">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <i class="fab fa-twitter"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                    </li>
                    <!-- /social contacts -->
                </ul>
                <!-- /contacts -->
            </div>
        </div>

        <div id="hero">
            <Nav 
            :navLinks="navLinks" />

            <img src="../assets/images/bg-parallax.png" alt="">

            <div class="jumbotron-title">
                
            </div>

        </div>    


      
  </header>
</template>

<script>
import Nav from './Nav';

export default {
    name: "Header",
    data: function() {
        return {
            openingTimes: "Mon - Sat - 9:00 - 18:00",
            phone: "+1 (305) 1234-5678" ,
            contactMail: "Hello@example.com",
            navLinks: [
                {
                    name: "Home",
                    url: ""
                },
                {
                    name: "Services",
                    url: ""
                },
                {
                    name: "About",
                    url: ""
                },
                {
                    name: "Projects",
                    url: ""
                },
                {
                    name: "Results",
                    url: ""
                }
            ]
        }
    },
    components: {
        Nav
    }

}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

header {
    height: 100vh;

    .info-bar {
        height: 40px;
        background-color: $bigStone;
        color: $pumice;
        display: flex;
        align-items: center;
        font-size: 11px;

        a {
            color: $pumice;
        }

        .nav-contacts {
            & > li {
                margin: 0 10px;

                i {
                    margin: 0 5px;
                }
            }
        }
    }
    
    #hero {
        height: calc(100% - 40px);
        background-color: lightcyan;

        img {
            height: 100%;
            width: 110%;
            object-fit: cover;
        }
    }
}

</style>