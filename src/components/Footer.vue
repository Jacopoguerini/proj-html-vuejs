<template>
    <footer>
        <FooterColumns
        :about="about"
        :services="services"
        :support="support"
        :contacts="contacts" />

        <div class="footer-bar">
            <div class="container">
                <span>Enjoy the low price. We are tracking any intention of piracy.</span>
                <span>&copy; 2020 NEXGEN is proudly powered by <a href="#">Codings</a>.</span>
            </div>
        </div>
    </footer>
</template>

<script>
import FooterColumns from './Footer-columns';

export default {
    name: "Footer",
    components: {
        FooterColumns
    },
    props: {
        "contacts": Object
    },
    data: function() {
        return {
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
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

    footer {
        background-color: $shark;
        color: $pumice;

        .footer-bar {
            background-color: $woodSmoke;
            height: 70px;

            .container {
                height: 100%;
                font-size: 11px;
                display: flex;
                justify-content: space-between;
                align-items: center;

                a {
                    text-decoration: none;
                    color: $blueLagoon;
                    
                    &:hover {
                        text-decoration: underline;
                    }
                }
            }
        }
    }

</style>