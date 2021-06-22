<template>
    <section id="projects">
        <div class="container">
            <h5>we do more for everyone</h5>
            <h2>Action &#38; <span class="span-highlight">Projects</span></h2>

            <ul class="list-inline">
                <li
                :class="(activeIndex == undefined) ? 'active' : ''"
                @click="selectAll()">
                    All
                </li>
                <li
                v-for="(project, index) in projects"
                :key="index"
                :class="(index == activeIndex) ? 'active' : ''"
                @click="selectProject(index)">
                    {{ project.sector }}
                </li>
            </ul>

            <div class="projects-list">

                <div class="project"
                v-for="(project, index) in selectedProjects"
                :key="index"
                :style="{ backgroundImage: 'url(' + project.backgroundPath + ')' }">
                    <div class="layover"></div>
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
            activeIndex: undefined,
            selectedProjects: this.projects
        }
    },
    methods: {
        selectAll: function() {
            this.activeIndex = undefined;
            this.selectedProjects = this.projects;
            document.getElementById("projects").scrollIntoView();
        },
        selectProject: function(newIndex) {
            this.activeIndex = newIndex;
            this.filterProjects();       
        },
        filterProjects: function() {
            this.selectedProjects = this.projects.filter(element => {
                if (this.activeIndex != undefined) {
                    return element.id == (this.activeIndex + 1);
                }
            });
        }

        
    }

}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

    #projects {
        min-height: 100vh;
        padding: 100px 0;

        h2 {
            color: $bigStone;
        }

        h2, h5 {
            text-align: center;
        }

        .list-inline {
            text-align: center;
            margin-bottom: 20px;

            li {
                text-transform: uppercase;
                cursor: pointer;
                margin: 0 10px;
                padding: 8px;
                font-size: 12px;
                color: $gravel;
                font-weight: 500;
            }
            .active {
                color: $blueLagoon;
                background-color: #d5e7e8;
            }
        }

        .projects-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: flex-start;
            align-items: center;
        }

        .project {
            width: calc((100% / 3) - 20px);
            height: 280px;
            padding: 35px 20px;
            margin: 10px;
            text-align: center;
            font-size: 18px;
            color: $greyNurse;
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            background-size: cover;
            overflow: hidden;
            border-radius: 10px;
            position: relative;
            
            & > * {
                z-index: 2;
            }
        }

    }

</style>