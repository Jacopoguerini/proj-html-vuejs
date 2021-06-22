<template>
  <main>
        <!-- Services -->
        <Services 
        :services="services"/>
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

        <!-- Projects -->
        <Projects 
        :projects="projects"/>
        <!-- /Projects -->
  </main>
</template>

<script>
import Services from './ServicesList';
import Projects from './Projects';

export default {
    name: "Main",
    components: {
        Services,
        Projects
    },
    data: function() {
        return {
            services: [
                {
                    name: "Audit & Assurance",
                    path: require("../assets/svgs/svg-1.svg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    name: "Financial Advisory",
                    path: require("../assets/svgs/svg-2.svg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    name: "Analytics & M&A",
                    path: require("../assets/svgs/svg-3.svg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    name: "Middle Marketing",
                    path: require("../assets/svgs/svg-4.svg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    name: "Legal Consulting",
                    path: require("../assets/svgs/svg-5.svg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },  
                {
                    name: "Regulatory Risk",
                    path: require("../assets/svgs/svg-6.svg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
                }
            ],
            projects: [
                {
                    sector: "All"
                },
                {
                    sector: "Institutional",
                    title: "Academic professional program in social media"
                },
                {
                    sector: "Social",
                    title: "President's speech at annual meeting"
                },
                {
                    sector: "Events",
                    title: "International business trip in Shanghai"
                },
                {
                    sector: "Innovation",
                    title: "Technology workshop with education team"
                },                   
                {
                    sector: "Environment",
                    title: "Donation of clothes and food to the partner NGO"
                },                    
                {
                    sector: "Technology",
                    title: "Confraternization to the procurement team"
                }                   
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

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