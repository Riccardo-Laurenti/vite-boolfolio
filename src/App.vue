<script>
import axios from 'axios';

const endpoint = 'http://127.0.0.1:8000/api/projects/';

import AppHeader from './components/AppHeader.vue';
import ProjectLists from './components/projects/ProjectLists.vue';
export default {
  components: { AppHeader, ProjectLists },

  data: () => ({ projects: [] }),
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
  <AppHeader />
  <main class="container my-4">
    <ProjectLists :projects="projects" />
  </main>
</template>



<style></style>