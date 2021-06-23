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
                <div class="project flip-card"
                v-for="(project, index) in selectedProjects"
                :key="index">
                    <div class="flip-card-inner">
                        <div
                        class="flip-card-front"
                        :style="{ backgroundImage: 'url(' + project.backgroundPath + ')' }">
                            <div class="layover"></div>
                            <h4>{{ project.title }}</h4>
                        </div>
                        <div class="flip-card-back">
                            <div class="layover"
                            :style="{ backgroundImage: 'url(' + project.backgroundPath + ')' }"></div>
                            <h4>{{ project.title }}</h4>
                            <h6>{{ project.summary }}</h6>
                            <a href="#">
                                <i class="fas fa-arrow-right"></i>
                            </a>
                        </div>
                    </div>
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
@import '../style/flipcard.scss';

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
            margin: 10px;
            text-align: center;
            font-size: 18px;
            color: $greyNurse;
            overflow: hidden;
            border-radius: 10px;
            position: relative;

            h4 {
                margin-bottom: 35px;
            }

            h6 {
                margin-top: 15px;
                margin-bottom: 30px;
            }

            a {
                position: absolute;
                top: 30px;
                right: 35px;
                color: $white;
            }

            h4, h6, a {
                z-index: 3;
            }

            .flip-card-front,
            .flip-card-back {
                display: flex;
                flex-direction: column;
                justify-content: flex-end;
                border-radius: 10px;
                padding: 0 15px;
                background-size: cover;
            }
            .flip-card-back {
                h4 {
                    margin-bottom: 0;
                }

                .layover {
                    filter: blur(5px);
                    background-size: cover;
                    box-shadow:inset 0 0 0 2000px rgba(0, 0, 0, 0.6)
                }
            }
        }

    }

</style>