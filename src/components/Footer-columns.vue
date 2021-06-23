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

        <!-- about -->
        <div class="footer-col list">
            <h4>About</h4>
            <ul>
                <li v-for="(item, index) in about" :key="index">
                    <i class="fas fa-chevron-right"></i>
                    <a :href="item.url">{{ item.name }}</a>
                </li>
            </ul>
        </div>
        <!-- /about -->

        <!-- services -->
        <div class="footer-col list">
            <h4>Services</h4>
            <ul>
                <li v-for="(item, index) in services" :key="index">
                    <i class="fas fa-chevron-right"></i>
                    <a :href="item.url">{{ item.name }}</a>
                </li>
            </ul>
        </div>
        <!-- /services -->

        <!-- support -->
        <div class="footer-col list">
            <h4>Support</h4>
            <ul>
                <li v-for="(item, index) in support" :key="index">
                    <i class="fas fa-chevron-right"></i>
                    <a :href="item.url">{{ item.name }}</a>
                </li>
            </ul>
        </div>
        <!-- /support -->
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


    .container {
        display: flex;
        justify-content: space-between;
        align-items: stretch;
        

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

        .list {
            background-color: rgba(80, 79, 81, 0.2);
            justify-content: center;
            border-radius: 10px;
            padding-left: 25px;
            
            ul {
                margin-bottom: 0;

                li {
                    margin-bottom: 10px;

                    i {
                        margin-right: 10px;
                        color: $pumice;
                    }
                    a {
                        text-decoration: none;
                        color: $pumice;
                        font-size: 13px;

                        &:hover {
                            text-decoration: underline;
                        }
                    }
                }
            }

            h4 {
                margin-bottom: 20px;
                font-size: 20px;
                color: $white;
            }
        }
    }

</style>