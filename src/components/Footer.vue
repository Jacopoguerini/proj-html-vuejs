<template>
    <footer>
        <FooterColumns
        :contacts="contacts"
        :about="about"
        :services="services"
        :support="support" />

        <div class="footer-bar">
            <div class="container">
                <span>Enjoy the low price. We are tracking any intention of piracy.</span>
                <span>&copy; 2020 NEXGEN is proudly powered by <a href="#">Codings</a>.</span>
            </div>

            <div class="arrow-top" @click="goToTop()">
                <i class="fas fa-arrow-up"></i>
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
        "contacts": Object,
        "about": Array,
        "services": Array,
        "support": Array
    },
    methods: {
        goToTop: function() {
            document.getElementById('home').scrollIntoView();
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
            position: relative;

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

            .arrow-top {
                width: 50px;
                height: 50px;
                cursor: pointer;
                position: absolute;
                right: 30px;
                top: 50%;
                color: $woodSmoke;
                background-color: rgba(80, 79, 81, 0.2);
                padding: 15px;
                font-size: 20px;
                border-radius: 50%;
                transform: translateY(-50%);
                display: flex;
                align-items: center;
                justify-content: center;
                transition: background-color 0.2s;

                &:hover {
                    background-color: $pumice;
                }
            }
        }
    }

</style>