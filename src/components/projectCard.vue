<template>
  <div class="card">
    <div class="card-content">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
      <div class="tech-tags">
        <span v-for="(tech, index) in technologies" :key="index" class="tech-tag">{{ tech }}</span>
      </div>
      <div class="card-links">
        <a :href="codeLink" target="_blank" class="card-link">See code</a>
        <a :href="liveLink" target="_blank" class="card-link" v-if="liveLink">Visit page</a>
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
.card {
  width: 100%;
  transition: all 0.2s ease-in-out;
  border-radius: 8px;
  z-index: 999;
}

.card:hover {
  transform: translateY(-2px);
  background-color: #061938;
  box-shadow: 2px 1px rgba(0, 0, 0, 0.306);
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
  background-color: #047d6172;
  color: #11cfc8;
  padding: 6px 10px;
  margin: 0 8px 4px 0;
  border-radius: 12px;
  font-size: 13px;
  font-weight: 700;
}

.card-links {
  display: flex;
  justify-content: space-between;
}

.card-link {
  text-decoration: none;
  color: #11cfc8;
  font-weight: bold;
  font-size: 14px;
}

.card-link:hover {
  text-decoration: underline;
}

@media (max-width: 1000px) {
  .card:hover {
    background-color:#03132d;
    box-shadow: none;
  }
  .card-content{
    padding: 16px 0;
  }
}
</style>