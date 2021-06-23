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