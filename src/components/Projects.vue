<template>
    <section id="projects">
        <div class="container">
            <h5>we do more for everyone</h5>
            <h2>Action &#38; <span class="span-highlight">Projects</span></h2>

            <ul class="list-inline">
                <li
                v-for="(project, index) in projects"
                :key="index"
                :class="(index == activeIndex) ? 'active' : ''"
                @click="setActive(index)">
                    {{ project.sector }}
                </li>
            </ul>

            <div class="projects-list">
                <div class="project"
                v-for="(project, index) in projects"
                :key="index">
                    <h4>{{ project.title }}</h4>
                </div>
            </div>
        </div>

    </section>
</template>

<script>
export default {
    name: "Projects",
    props: {
        "projects": Array
    },
    data: function() {
        return {
            active: true,
            activeIndex: 0
        }
    },
    methods: {
        setActive: function(newIndex) {
            this.activeIndex = newIndex;
        },
    }

}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

    #projects {

        padding: 100px 0;

        h2 {
            color: $bigStone;
        }

        h2, h5 {
            text-align: center;
        }

        .list-inline {
            text-align: center;

            li {
                text-transform: uppercase;
                cursor: pointer;
                margin: 0 15px;
                padding: 8px;
                font-size: 14px;
                color: $gravel;
                font-weight: 500;
            }
            .active {
                color: $blueLagoon;
                background-color: #d5e7e8;
            }
        }

        .project
    }

</style>