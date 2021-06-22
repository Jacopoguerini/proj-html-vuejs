<template>

    <section class="container">

        <div class="footer-col">
            <img src="../assets/svgs/svg-7.svg" alt="NexGen Logo">
            <p>A functional HTML Template for Corporate &amp; Business.</p>
            <ul>
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
            <span class="btn btn-secondary">
                <a href="#contacts">
                    get in touch
                </a>
            </span>
        </div>
        
        <div class="footer-col">

        </div>

        <div class="footer-col">

        </div>

        <div class="footer-col">

        </div>
    </section>
</template>

<script>
export default {
    name: "FooterColumns",
    props: {
        "about": Array,
        "services": Array,
        "support": Array,
        "contacts": Object
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

    .footer-col {
        font-size: 12px;
        display: flex;
        flex-direction: column;
        align-items: flex-start;

        p {
            margin: 20px 0;
        }

        ul {
            margin-bottom: 20px;

            li {
                margin-bottom: 15px;

                i {
                    margin-right: 10px;
                }
            }
        }

        img {
            height: 40px;
        }

        .btn {
            padding:  8px 0;

            a {
                color: $white;
                font-size: 12px;
            }
        }
    }

</style>