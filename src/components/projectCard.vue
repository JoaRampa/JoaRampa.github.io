<template>
  <div class="card">
    <div class="card-image" :style="{ backgroundImage: `url(${image})` }"></div>
    <div class="card-content">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
      <div class="tech-tags">
        <span v-for="(tech, index) in technologies" :key="index" class="tech-tag">{{ tech }}</span>
      </div>
      <div class="card-links">
        <a :href="codeLink" target="_blank" class="card-link">Ver Código</a>
        <a :href="liveLink" target="_blank" class="card-link">Demo en Vivo</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    description: String,
    image: String,
    technologies: Array,
    codeLink: String,
    liveLink: String
  }
};
</script>

<style scoped>
/* Estilos generales */
.card {
  width: 100%;
  transition: all 0.3s ease-in-out;
  border-radius: 8px;
}

.card:hover {
  transform: translateY(-2px);
  background-color: #061938;
}

.card-image {
  background-size: cover;
  background-position: center;
  opacity: 0.8;
}

.card-content {
  padding: 16px 0;
  color: #ccd6f6;
}

h3 {
  font-size: 18px;
  margin: 0;
}

p {
  font-size: 14px;
  color: #8892b0;
  margin-bottom: 12px;
}

.tech-tags {
  margin-bottom: 12px;
}

.tech-tag {
  display: inline-block;
  background-color: #64ffda;
  color: #0a192f;
  padding: 4px 8px;
  margin-right: 8px;
  margin-bottom: 8px;
  border-radius: 4px;
  font-size: 12px;
}

.card-links {
  display: flex;
  justify-content: space-between;
}

.card-link {
  text-decoration: none;
  color: #64ffda;
  font-weight: bold;
  font-size: 14px;
}

.card-link:hover {
  text-decoration: underline;
}

@media (max-width: 1000px) {
  .card:hover {
    background-color:#03132d;
  }
}
</style>