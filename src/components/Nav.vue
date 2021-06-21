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

                <!-- get in touch button -->
                <li class="btn">
                    <a href="#">
                        get in touch
                    </a>
                </li>
                <!-- /get in touch button -->
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
        position: absolute;
        width: 100%;
        height: 70px;
        color: $gravel;
        display: flex;
        align-items: center;
        background-color: transparent;

        img {
            height: 30px;
        }

        a {
                text-transform: uppercase;    
                color: $gravel;
                margin: 0 10px;
                padding: 5px;
        }

        .navbar {
            font-size: 14px;
            font-weight: 600;            
        }
    }

</style>