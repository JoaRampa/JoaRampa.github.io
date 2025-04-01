<template>
  <nav class="navbar">
    <ul class="nav-links">
      <li>
        <a href="#about" class="link" @click.prevent="setActive('#about')" :class="{ active: activeLink === '#about' }">
          <span class="dash">&mdash;&mdash;</span>
          <span class="text">About</span>
        </a>
      </li>
      <li>
        <a href="#projects" class="link" @click.prevent="setActive('#projects')" :class="{ active: activeLink === '#projects' }">
          <span class="dash">&mdash;&mdash;</span>
          <span class="text">Projects</span>
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      activeLink: ''
    };
  },
  methods: {
    setActive(link) {
      this.activeLink = link;
      window.location.hash = link;
    }
  },
  mounted() {
    this.activeLink = window.location.hash || '#about';
    window.addEventListener('hashchange', () => {
      this.activeLink = window.location.hash;
    });
  }
};
</script>

<style>
.nav-links {
  list-style: none;
  padding: 0;
}

.link {
  display: flex;
  align-items: center;
  text-decoration: none;
  color: #dfd9d9;
  font-size: 1.1cqmax;
  transition: opacity 0.3s ease-in-out;
}

.dash {
  width: 20px;
  overflow: hidden;
  transition: width, opacity;
  opacity: 0.6;
  margin-right: 8px;
}

.link:hover .dash, .active .dash, 
.link:hover .text, .active .text {
  width: 30px;
  opacity: 1;
  filter: brightness(250%);
  font-weight: bold;
}

.active{
  font-weight: bold;
  filter: brightness(250%);
}
</style>