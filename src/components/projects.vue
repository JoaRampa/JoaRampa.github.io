<template>
  <div class="projects-container">
    <ProjectCard
      title="Nombre del Proyecto"
      description="Una breve descripción del proyecto que destaque sus características principales."
      image="URL_de_la_imagen_del_proyecto"
      :technologies="['Tecnología1', 'Tecnología2', 'Tecnología3']"
      codeLink="URL_del_repositorio_del_código"
      liveLink="URL_de_la_demo_en_vivo"
    />
    <ProjectCard
      title="Nombre del Proyecto"
      description="Una breve descripción del proyecto que destaque sus características principales."
      image="URL_de_la_imagen_del_proyecto"
      :technologies="['Tecnología1', 'Tecnología2', 'Tecnología3']"
      codeLink="URL_del_repositorio_del_código"
      liveLink="URL_de_la_demo_en_vivo"
    />
    <ProjectCard
      title="Nombre del Proyecto"
      description="Una breve descripción del proyecto que destaque sus características principales."
      image="URL_de_la_imagen_del_proyecto"
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