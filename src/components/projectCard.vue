<template>
  <div class="card">
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
  padding: 16px;
}

h3 {
  font-size: 18px;
  margin: 0;
}

p {
  font-size: 14px;
  opacity: 0.6;
  margin-bottom: 12px;
}

.tech-tags {
  margin-bottom: 12px;
}

.tech-tag {
  display: inline-block;
  background-color: #32d0ab;
  color: #0a192f;
  padding: 4px 8px;
  margin: 0 8px 4px 0;
  border-radius: 8px;
  font-size: 12px;
}

.card-links {
  display: flex;
  justify-content: space-between;
}

.card-link {
  text-decoration: none;
  color: #32d0ab;
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
  .card-content{
    padding: 16px 0;
  }
}
</style>