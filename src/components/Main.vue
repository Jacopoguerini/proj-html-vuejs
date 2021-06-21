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
                <h5>about the network</h5>
                <h2><span class="span-highlight">The</span> Company</h2>
            </div>
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
            color: $bigStone;
        }
    }

    #services {
        background-color: $greyNurse;

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
            }
        }

    }

</style>