<script>
import axios from 'axios';
import ProjectLists from '../components/projects/ProjectLists.vue';
const endpoint = 'http://127.0.0.1:8000/api/projects/';
export default {
    name: 'HomePage',
    components: { ProjectLists },
    data: () => ({
        projects: []
    }),
    methods: {
        fetchProjects() {
            axios.get(endpoint).then(res => { this.projects = res.data })
        }
    },
    created() {
        this.fetchProjects();
    }
};
</script>


<template>
    <ProjectLists :projects="projects" />
</template>





<style></style>