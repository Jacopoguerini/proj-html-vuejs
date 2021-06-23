<template>
    <nav>
        <div class="container">

            <!-- logo image -->
            <div class="image-logo">
                <a href="#home">
                    <img src="../assets/svgs/svg-7.svg" alt="NexGen Logo">
                </a>
            </div>
            <!-- /logo image -->

            <div class="nav-right">
                <ul class="navbar list-inline">
                    <li v-for="link in navLinks" :key="link.name">
                        <a :href="link.url">
                            {{ link.name }}
                        </a>
                    </li>
                </ul>

                <!-- get in touch button -->
                <span class="btn btn-primary">
                    <a href="#contacts">
                        get in touch
                    </a>
                </span>
                <!-- /get in touch button -->
            </div>
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
        z-index: 999;

        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;

            .nav-right {
                & > * {
                    display: inline-block;
                }

                ul {
                    li {
                        margin: 0 10px;

                        a:hover {
                            color: $pumice;
                        }
                    }
                }
            }
        }

        img {
            height: 30px;
        }

        a {
            text-transform: uppercase;    
            color: $gravel;
            padding: 5px;
        }

        .navbar {
            font-size: 14px;
            font-weight: 500;            
        }
    }

</style>