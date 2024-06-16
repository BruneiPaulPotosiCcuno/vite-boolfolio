<script>
import axios from 'axios';
import SingleProject from './SingleProject.vue';

export default {
    name: 'ProjectList',
    components:{
        SingleProject,
    },
    data() {
        return {
            projects: []
        };

    },
    methods: {

        getProjects() {
            axios.get('http://127.0.0.1:8000/api/posts')
                .then((response) => {
                    this.projects = response.data.results
                })
        }
    },
    mounted() {
        this.getProjects();
    },
}
</script>

<template>
    <div class="container">
        <h1>Questi sono tutti i post:</h1>
        <div class="row row-cols-3">
            <SingleProject v-for="project in projects" :projectDetails="project" :key="project.id"></SingleProject>
        </div>



    </div>
</template>

<style scoped lang="scss"></style>