<template>
  <main>
        <!-- Services -->
        <section id="services">
            <div class="container">
                <h5>our business areas</h5>
                <h2>Excellence in <span class="span-highlight">Services</span></h2>
                <div class="subtitle">
                    <p>We are leaders in providing consultancy with a set of cutting-edge technologies and a team of experienced and renowned professionals. These are some options that you can hire.</p>
                    <span class="btn btn-primary">
                        <a href="#">see all</a>
                    </span>
                </div>

                <div class="services-container">

                    <div class="service">
                        <img src="../assets/svgs/svg-1.svg" alt="">
                        <h3>Audit & Assurance</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        <i class="fas fa-arrow-right"></i>
                    </div>

                    <div class="service">
                        <img src="../assets/svgs/svg-2.svg" alt="">
                        <h3>Financial Advisory</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        <i class="fas fa-arrow-right"></i>
                    </div>

                    <div class="service">
                        <img src="../assets/svgs/svg-3.svg" alt="">
                        <h3>Analytics and M&A</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        <i class="fas fa-arrow-right"></i>
                    </div>

                    <div class="service">
                        <img src="../assets/svgs/svg-4.svg" alt="">
                        <h3>Middle Marketing</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        <i class="fas fa-arrow-right"></i>
                    </div>

                    <div class="service">
                        <img src="../assets/svgs/svg-5.svg" alt="">
                        <h3>Legal Consulting</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        <i class="fas fa-arrow-right"></i>
                    </div>

                    <div class="service">
                        <img src="../assets/svgs/svg-6.svg" alt="">
                        <h3>Regulatory Risk</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        <i class="fas fa-arrow-right"></i>
                    </div>
        
                </div>

            </div>
        </section>
        <!-- /Services -->

        <!-- the Company -->
        <section id="company">
            <div class="container">

                <div class="bullets" id="top">
                    <img src="../assets/bullets.png" alt="">
                </div>

                <div class="about">
                    <h5>about the network</h5>
                    <h2><span class="span-highlight">The</span> Company</h2>
                    <p>For 12 years we have been providing audit and warranty, financial advice, risk advice, taxes and related services to select clients.</p>

                    <div class="list">
                        <div>

                            <span>
                                <i class="fas fa-award"></i>
                                <h4>Tradition</h4>
                            </span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>

                        <div>
                            <span>
                                <i class="fas fa-lock"></i>
                                <h4>Tradition</h4>
                            </span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>

                        <div>
                            <span>
                                <i class="far fa-edit"></i>
                                <h4>Certificate</h4>
                            </span>
                            
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>

                        <div>
                            <span>
                                <i class="fas fa-graduation-cap"></i>
                                <h4>Expertise</h4>
                            </span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>
                    </div>

                    <div class="buttons">
                        <span class="btn btn-primary">
                            <a href="#">
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

                <div class="bullets" id="bottom">
                    <img src="../assets/bullets.png" alt="">
                </div>
            </div>
            
            <img src="../assets/images/about-4.jpg" alt="">
        </section>
        <!-- /the Company -->
  </main>
</template>

<script>

export default {
    name: "Main"
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

    section {
        padding: 70px 0;

        h2 {
            margin: 25px 0;
        }
    }

    #services {
        background-color: $greyNurse;

        h2 {
            color: $bigStone;
        }

        .subtitle {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        h3 {
            color: $shark;
            font-weight: 700;
            margin: 20px 0;
        }

        p {
            color: $gravel;
            display: inline-block;
            width: 75%;
        }

            .services-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;

        }

        .service {
            width: 32%;
            background-color: $white;
            padding: 30px;
            margin: 20px 0;
            border-radius: 10px;
            position: relative;

            img {
                width: 30px;
            }

            i {
                position: absolute;
                color: $blueLagoon;
                opacity: 0.6;
                font-size: 20px;
                top: 50px;
                right: 30px;
                transform: translate(-50%, -50%);
                cursor: pointer;
            }
        }

    }

    #company {
        color: $pumice;
        background-color: $woodSmoke;
        position: relative;

        .span-highlight {
            color: $white;
            background-color: rgba(3, 132, 132, 0.2);
        }

        h2,
        h4 {
            color: $white;
        }
        h4 {
            font-size: 20px;
            display: inline-block;
        }

        & > img {
            height: 100%;
            width: 50%;
            object-fit: cover;
            position: absolute;
            top: 0;
            right: 0;
        }

        .about {
            width: 49%;
            

            .list {
                display: flex;
                flex-wrap: wrap;
                margin: 50px 0 20px 0;

                div {
                    width: calc(50% - 10px);
                    display: flex;
                    flex-direction: column;
                    align-items: flex-start;
                    justify-content: center;
                    margin-bottom: 50px;

                    span {
                        margin-bottom: 25px;
                    }

                    i {
                        color: $blueLagoon;
                        margin-right: 10px;
                    }
                }
            }
            
            .buttons {
                
                .btn {
                    margin: 0 15px;
                }
                .btn-primary {
                    margin-left: 0;
                }
            }
        }

        .bullets {
            width: 120px;
            height: 50px;
            position: absolute;
            overflow: hidden;
            left: 50%;
            transform: translateX(-50%);
            z-index: 1000;
            opacity: 0.5;

            img {
                width: 100%;
                object-fit: cover;
            }
        }
        .bullets#top {
            top: -25px;
        }
        .bullets#bottom {
            bottom: -25px;
        }
    }

</style>