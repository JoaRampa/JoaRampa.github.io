<template>
  <div class="projects-container">
    <ProjectCard
      title="Crypcreate"
      description="Cryptocurrency wallet. Buying, selling, transaction history, and investment analysis."
      :technologies="['Vue.js', 'Vuex', 'Axios']"
      codeLink="https://github.com/JoaRampa/cryptowallet-vuejs"
      liveLink="https://lab3-crypcreate.netlify.app/"
    />
    <ProjectCard
      title="Nombre del Proyecto"
      description="Una breve descripción del proyecto que destaque sus características principales."
      :technologies="['Tecnología1', 'Tecnología2', 'Tecnología3']"
      codeLink="URL_del_repositorio_del_código"
      liveLink="URL_de_la_demo_en_vivo"
    />
    <ProjectCard
      title="Nombre del Proyecto"
      description="Una breve descripción del proyecto que destaque sus características principales."
      :technologies="['Tecnología1', 'Tecnología2', 'Tecnología3']"
      codeLink="URL_del_repositorio_del_código"
      liveLink="URL_de_la_demo_en_vivo"
    />
  </div>
</template>

<script>
import ProjectCard from './projectCard.vue';

export default {
  components: {
    ProjectCard
  }
};
</script>

<style scoped>
.projects-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>