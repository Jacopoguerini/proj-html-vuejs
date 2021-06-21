<template>
    <div class="services-container">

        <div class="service" v-for="(service, index) in services" :key="index">
            <img :src="service.imageName" :alt="service.name">
            <h3>{{ service.name }}</h3>
            <p>{{ service.summary }}</p>
        </div>
        
    </div>
</template>

<script>
export default {
    name: "Services",
    props: {
        "services": Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

    .services-container {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;

    }

    .service {
        width: 32%;
        height: 300px;
        background-color: $white;
        padding: 20px 0;
        margin: 20px 0;

    }

</style>