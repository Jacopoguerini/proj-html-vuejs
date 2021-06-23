<template>
    <header id="home">
        <div class="info-bar">
            <div class="container">
                <!-- opening times -->
                <div class="nav-opening-times">
                    <i class="fas fa-clock"></i>
                    <span>
                    Open Hours: {{ contacts.openingTimes }}
                    </span>
                </div>
                <!-- /opening times -->

                <!-- contacts -->
                <ul class="nav-contacts list-inline">
                    <!-- phone number -->
                    <li>
                        <i class="fas fa-phone-alt"></i>
                        <span>{{ contacts.phone }}</span>
                    </li>
                    <!-- /phone number -->

                    <!-- mail -->
                    <li>
                        <i class="fas fa-envelope"></i>
                        <span>{{ contacts.contactMail }}</span>
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

            <div class="image-layer">
                <div class="jumbotron-title">
                    
                    <h1>Ready <span class="span-highlight">Team</span></h1>
                    
                    <p>No matter what your company needs, we will be ready to assist you in the best possible way</p>
                    
                    <div class="buttons">
                        <span class="btn btn-primary">
                            <a href="#contacts">
                            get in touch
                            </a>
                        </span>
                        <span class="btn btn-secondary">
                            <a href="#">
                            read more
                            </a>
                        </span>
                    </div>
                </div>

                <div class="slider">
                    <!-- <div class="slider-dot"
                    v-for="(div, index) in 3"
                    :key="index"></div> -->
                    <div class="slider-dot"></div>
                    <div class="slider-dot active"></div>
                    <div class="slider-dot"></div>                    
                </div>
            </div>
        </div>    
  </header>
</template>

<script>
import Nav from './Nav';

export default {
    name: "Header",
    components: {
        Nav
    },
    props: {
        "contacts": Object,
        "navLinks": Array
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

        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        a {
            color: $pumice;
        }

        .nav-contacts {
            & > li {
                margin: 0 10px;

                &:hover {
                    a {
                        color: $white;
                    }
                }

                i {
                    margin: 0 5px;
                }
            }
        }
    }
    
    #hero {
        height: calc(100% - 40px);
        background-color: $white;

        .image-layer {
            height: 100%;
            width: 100%;
            margin: 0 auto;
            position: relative;
            background-image: url("../assets/images/bg-parallax.png");
            background-position: center;
            background-size: 190%;
            background-repeat: no-repeat;

            .slider{
                position: absolute;
                height: auto;
                width: auto;
                top: 50%;
                right: 0;
                transform: translateY(-50%);
                margin-right: 25px;
                
                .slider-dot{
                    height: 25px;
                    width: 7px;
                    border-radius: 5px;
                    background-color: transparent;
                    margin: 5px;
                    border: 1px solid $elm;
                    cursor: pointer;

                    &:hover {
                        background-color: $fountainBlue;
                    }
                }

                .active {
                    background-color: $elm;
                }

            }

        }

        .jumbotron-title {
            text-align: center;
            width: 30%;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);

            & > * {
                margin: 10px 0;
            }

            .btn,
            .btn-secondary {
                margin: 0 15px;
            }

            p {
                color: $gravel;
                padding: 25px;
            }
        }
    }
}

</style>