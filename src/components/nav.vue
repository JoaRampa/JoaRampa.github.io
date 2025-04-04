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
.navbar {
  margin-top: 4rem
}

.nav-links {
  list-style: none;
  padding: 0;
  width: 180px;
}

.link {
  display: flex;
  align-items: center;
  text-decoration: none;
  color: #dfd9d9;
  transition: all 0.5s ease-in-out;
  text-transform: uppercase;
  font-weight: 700;
}

.text {
  transition: all .8s ease-in-out;
}

.dash {
  width: 40px;
  overflow: hidden;
  transition: all .8s ease-in-out;
  opacity: 0.6;
}

.link:hover .dash, .active .dash, 
.link:hover .text, .active .text {
  transition: opacity 0.8s ease-in-out;
  opacity: 1;
  filter: brightness(250%);
  font-weight: bold;
  transform: translateY(-1px);
}

.active{
  font-weight: bold;
  filter: brightness(250%);
  margin:0;
}
</style>