<script>
export default {
    name: 'ProjectCard',
    props: { project: Object }
};
</script>


<template>
    <div class="card my-4">
        <div class="card-header">
            <h1>{{ project.title }}</h1>
        </div>
    </div>
    <div class="card my-4">
        <div class="card-body">
            <p>{{ project.content }}</p>
        </div>
    </div>
    <div class="card-footer d-flex justify-content-between align-items-center">
        <address>{{ project.author }}</address>
    </div>
</template>





<style></style>