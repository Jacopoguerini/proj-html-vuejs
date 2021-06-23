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

        <!-- Results -->
        <section class="numbers">
            <section id="results">
                <div class="container">
                    
                    <h5>what we are doing</h5>
                    <h2><span class="span-highlight">Results</span> in Numbers</h2>
                    <ul class="data">
                        <li v-for="(result, index) in results" :key="index">
                            <h4>{{result. number}}</h4>
                            <h5>{{ result.name }}</h5>

                        </li>
                    </ul>

                    <div class="partner-logos">
                        <ul class="logo-list">
                            <li v-for="(partner, index) in partners" :key="index">
                                <img :src="partner.logoUrl" :alt="partner.name">
                            </li>
                        </ul>
                    </div>
                </div>


            </section>
        </section>
        <!-- /Results -->

        <!-- Contacts -->
        <section id="contacts">
            <div class="container">
                <div class="form">

                    <h5>send a message</h5>
                    <h2>Get in <span class="span-highlight">Touch</span></h2>
                    <p>We will respond to your message as soon as possible.</p>
                    <form>
                        
                        <input type="text" placeholder="Name">
                        <input type="email" placeholder="Email">
                        <input type="tel" placeholder="Phone">
                        <select name="More Info" id="">
                            <option value="">More info</option>
                            <option value="1">Info 1</option>
                            <option value="2">Info 2</option>
                            <option value="3">Info 3</option>                                                        
                            <option value="4">Info 4</option>                            
                        </select>
                        <textarea type="text" placeholder="Message" rows="7"></textarea>

                        <button class="btn btn-primary">
                            send
                        </button>
                    </form>
                </div>
                <div class="contacts">

                    <h3>Example Inc.</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                    <p>Odit optio doloribus nesciunt commodi eligendi.</p>

                    <ul class="info-list">
                        <li>
                            <i class="fas fa-phone-alt"></i>
                            <span>{{ contacts.phone }}</span>
                        </li>
                        <li>
                            <i class="fas fa-envelope"></i>
                            <span>{{ contacts.contactMail }}</span>
                        </li>
                        <li>
                            <i class="fas fa-map-marker-alt"></i>
                            <span>{{ contacts.address }}</span>
                        </li>
                    </ul>

                    <a class="btn btn-secondary" @click="showMap()">
                        view map
                    </a>

                    <div id="map">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3017.186268079908!2d-74.13503908472748!3d40.86778627931521!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c2fecf01cf914d%3A0x3ee97a91f650bf73!2s897%20Main%20Ave%2C%20Passaic%2C%20NJ%2007055%2C%20Stati%20Uniti!5e0!3m2!1sit!2sit!4v1624432585511!5m2!1sit!2sit" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                        
                        <div class="close-map" @click="closeMap()">
                            <i class="fas fa-times"></i>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- /Contacts -->
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
    props: {
        "contacts": Object
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
                    id: 1,
                    sector: "Institutional",
                    title: "Academic professional program in social media",
                    backgroundPath: require('../assets/images/project-1.jpg'),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    id: 2,
                    sector: "Social",
                    title: "President's speech at annual meeting",
                    backgroundPath: require("../assets/images/project-2.jpg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    id: 3,                    
                    sector: "Events",
                    title: "International business trip in Shanghai",
                    backgroundPath: require("../assets/images/project-3.jpg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."                    
                },
                {
                    id: 4,                    
                    sector: "Innovation",
                    title: "Technology workshop with education team",
                    backgroundPath: require("../assets/images/project-4.jpg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."                    
                },                   
                {
                    id: 5,                    
                    sector: "Environment",
                    title: "Donation of clothes and food to the partner NGO",
                    backgroundPath: require("../assets/images/project-5.jpg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },                    
                {
                    id: 6,                    
                    sector: "Technology",
                    title: "Confraternization to the procurement team",
                    backgroundPath: require("../assets/images/project-6.jpg"),
                    summary: "Lorem ipsum dolor sit amet consectetur adipisicing elit."                    
                }                   
            ],
            results: [                
                {
                    name: "Certifications",
                    number: 128
                },
                {
                    name: "Employees",
                    number: 230
                },
                {
                    name: "Customers",
                    number: 517
                },   
                {
                    name: "Countries Served",
                    number: 94
                }                           
            ],
            partners: [
                {
                    name: "jQuery",
                    logoUrl: require('../assets/images/logo-4.png'),
                    url: ""
                },
                {
                    name: "less",                    
                    logoUrl: require('../assets/images/logo-5.png'),
                    url: ""
                },
                {
                    name: "WooCommerce",                    
                    logoUrl: require('../assets/images/logo-1.png'),
                    url: ""
                },
                {
                    name: "WordPress",                    
                    logoUrl: require('../assets/images/logo-2.png'),
                    url: ""
                },
                {
                    name: "Pingdom",
                    logoUrl: require('../assets/images/logo-3.png'),
                    url: ""
                },
                {
                    name: "jQuery",
                    logoUrl: require('../assets/images/logo-4.png'),
                    url: ""
                }                                                                  
            ]
        }
    },
    methods: {
        showMap: function() {
            document.getElementById('map').style.display = "block";
            document.getElementById('contacts').scrollIntoView();
        },
        closeMap: function() {
            document.getElementById('map').style.display = "none";            
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

    #results {
        text-align: center;
        padding: 100px 0;
        padding-bottom: 300px;
        position: relative;

        h2 {
            color: $white;
            margin-bottom: 100px;
        }
        .span-highlight {
            color: $white;
            background-color: rgba(3, 132, 132, 0.2);
        }

        .data {
            display: flex;
            justify-content: space-around;
            align-items: center;

            & > li {
                display: inline-block;

                h4 {
                    color: $elm;
                    font-size: 30px;
                    margin-bottom: 10px;
                }
                h5 {
                    color: $white;
                    text-transform: none;
                    font-size: 18px;
                }
            }
        }

        .partner-logos {
            background-color: $shark;
            padding: 70px 0;
            height: 200px;
            width: 100%;
            position: absolute;
            bottom: 0;
            left: 0;
            display: flex;
            align-items: center;
            justify-content: center;

            .logo-list {  
                display: flex;          

                li {
                    height: 20px;

                    img {
                        filter: invert(60%);
                        height: 100%;
                        margin: 0 30px;
                    }
                }
            }
        }
    }
    .numbers {
        padding: 0 0;
        background-image: url("../assets/images/bg-7.jpg");
        background-size: cover;
        background-position: center;
    }

    #contacts {
        position: relative;

        .container {
            display: flex;
            justify-content: space-between;

            .form {
                width: 60%;

                form {
                    margin-top: 50px;
                }

                input,
                select,
                textarea {
                    outline: none;
                    background-color: rgba(188, 190, 188, 0.4);
                    border-radius: 3px;  
                    border: none;
                    padding: 10px;
                }

                input,
                select {
                    width: calc(50% - 5px);
                    margin-bottom: 10px;         
                }
                input[type="email"],
                select {
                    margin-left: 10px;
                }
                input[type="text"] {
                    background-image: url('../assets/images/image (1).png');
                    background-repeat: no-repeat;
                    background-position: 97%;
                }

                textarea {
                    resize: none;
                    width: 100%;
                    margin-bottom: 30px;
                }

                input::placeholder,
                select,
                textarea::placeholder {
                    font-family: "Montserrat";
                    color: $gravel;
                }

                button {
                    font-size: 13px;
                    padding: 10px 20px;
                }
            }

            .contacts {
                width: 35%;
                display: flex;
                flex-direction: column;
                align-items: flex-start;

                h3,
                p {
                    margin-bottom: 25px; 
                }

                .info-list {
                    margin-bottom: 20px;
                
                    li {
                        margin-bottom: 20px;
                        i {
                            color: $blueLagoon;
                            padding: 10px;
                            border-radius: 50%;
                            background-color: #d5e7e8;
                            margin-right: 10px;
                        }
                        span {
                            color: $blueLagoon;
                        }
                    }
                }
            }
        }

        h2,
        h3 {
            color: $bigStone;
        }
        p {
            color: $gravel;
        }

        #map {
            display: none;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            box-shadow: 0 0 10px $shark;

            .close-map {
                width: 15px;
                height: 15px;
                position: absolute;
                top: -12px;
                right: -12px;
                display: flex;
                justify-content: center;
                align-items: center;
                padding: 10px;
                color: $white;
                background-color: $gravel;
                border-radius: 50%;
                box-shadow: 0 0 10px $shark;
                cursor: pointer;
                border: 3px solid $white;
            }
        }
    }

</style>