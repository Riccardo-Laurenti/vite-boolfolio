<script>



import HomePage from './pages/HomePage.vue';
import AppHeader from './components/AppHeader.vue';
//import ProjectLists from './components/projects/ProjectLists.vue';

export default {
  components: { AppHeader, HomePage },


};
</script>


<template>
  <AppHeader />
  <main class="container my-4">
    <HomePage />
  </main>
</template>



<style></style>