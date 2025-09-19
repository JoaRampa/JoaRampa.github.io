<template>
  <div class="projects-container">
    <ProjectCard
      title="LB Stock reform"
      description="Reworked stock app for the web. (Work still in process!)"
      :technologies="['Vue 3', 'SupaBase', 'JavaScript', 'CSS', 'UX/UI']"
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
      title="C# ASP.NET Application"
      description="ASP.NET MVC application with authentication and order management, using Entity Framework and AppDbContext. Developed as a university project."
      :technologies="['C#', 'ASP.NET MVC', 'Entity Framework', 'AppDbContext', 'SQL Server']"
      codeLink="https://github.com/JoaRampa/cSharp-aspNet-MVC"
    />
    <ProjectCard
      title="LB Stock"
      description="Stock application for the LB cleaning supplies company. Developed in accordance with the university thesis."
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