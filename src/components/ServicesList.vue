<template>

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
                <div class="service" v-for="(service, index) in services" :key="index">
                    <img :src="service.path" alt="">
                    <h3>{{ service.name }}</h3>
                    <p>{{ service.summary }}</p>
                    <a href="#">
                        <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
            </div>

        </div>
    </section>

</template>

<script>
export default {
    name: "Services",
    props: {
        "services": Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

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
                color: $bigStone;
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

                &:hover {
                    i {
                        opacity: 1;
                        background-color: $fountainBlue;
                        border-radius: 50%;
                    }
                }

                img {
                    width: 30px;
                }

                i {
                    position: absolute;
                    color: $blueLagoon;
                    opacity: 0.6;
                    font-size: 20px;
                    top: 35px;
                    right: 5px;
                    transform: translate(-50%, -50%);
                    cursor: pointer;
                    padding: 5px;
                    transition: opacity 0.2s, background-color 0.2s, border-radius 0.2s;
                }
            }

    }
</style>