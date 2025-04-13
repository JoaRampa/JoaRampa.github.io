<template>
  <div class="projects-container">
    <ProjectCard
      title="LB Stock reform"
      description="Aplicacion de stock reformada para la web"
      :technologies="['Vue', 'SupaBase']"
      codeLink="https://github.com/JoaRampa/TUP-Final"
      liveLink="https://lbstock-tesi.netlify.app/"
    />
    <ProjectCard
      title="Crypcreate"
      description="Cryptocurrency wallet. Buying, selling, transaction history, and investment analysis."
      :technologies="['Vue', 'Vuex', 'Axios']"
      codeLink="https://github.com/JoaRampa/cryptowallet-vuejs"
      liveLink="https://lab3-crypcreate.netlify.app/"
    />
    <ProjectCard
      title="LB Stock"
      description="Aplicacion de stock para la empresa LB de articulos de limpieza. Hecha en concordancia con la tesis de la universidad."
      :technologies="['Vue', 'Express.js', 'SQLite3', 'Electron.js', 'Node.js']"
      codeLink="https://github.com/JoaRampa/lb_stock"
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