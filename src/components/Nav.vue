<template>
    <nav>
        <div class="container flex-spbt-centre">

            <!-- logo image -->
            <div class="image-logo">
                <a href="#">
                    <img src="../assets/logo.png" alt="NexGen Logo">
                </a>
            </div>
            <!-- /logo image -->

            <ul class="navbar list-inline">
                <li v-for="link in navLinks" :key="link.name">
                    <a :href="link.url">
                        {{ link.name }}
                    </a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>

export default {
    name: "Nav",
    props: {
        "navLinks": Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

    nav {
        height: calc(100% - 30px);
        color: $gravel;
        display: flex;
        align-items: center;
        background-color: green;

        img {
            height: 40px;
        }

        .navbar {
            font-size: 14px;
            font-weight: 600;

            a {
                text-transform: uppercase;    
                color: $gravel;
                margin: 0 10px;
                padding: 10px 15px;
            }
        }
    }

</style>