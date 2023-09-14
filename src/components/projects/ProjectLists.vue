<script>
import ProjectCard from './ProjectCard.vue';
export default {
    name: 'ProjectLists',
    components: { ProjectCard },
    props: { projects: Array }
};
</script>


<template>
    <section>
        <h1 class="text-center my-4">My projects</h1>
        <div v-if="projects.length">
            <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
        </div>
        <h2 v-else>Non ci sono progetti da visualizzare</h2>
    </section>
</template>





<style></style>