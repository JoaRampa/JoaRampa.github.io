<template>
  <nav class="navbar">
    <ul class="nav-links">
      <li>
        <a href="#about" class="link"
          @click.prevent="setActive('#about')"
          @mouseenter="hoverLink = '#about'"
          @mouseleave="hoverLink = ''"
          :class="{ active: activeLink === '#about' }">
          <span class="dash" v-html="'&mdash;&mdash;&mdash;&mdash;'"></span>
          <span class="text">About</span>
        </a>
      </li>
      <li>
        <a href="#projects" class="link" 
          @click.prevent="setActive('#projects')"
          @mouseenter="hoverLink = '#projects'"
          @mouseleave="hoverLink = ''" 
          :class="{ active: activeLink === '#projects' }">
          <span class="dash" v-html="'&mdash;&mdash;&mdash;&mdash;'"></span>
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
      activeLink: '',
      hoverLink: ''
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
  width: 200px;
}

.nav-links li {
  margin-bottom: .5rem;
}

.link {
  display: flex;
  align-items: center;
  text-decoration: none;
  color: #dfd9d9;
  transition: all 0.5s ease-in-out;
  text-transform: uppercase;
  font-weight: 700;
  gap: .75rem;
}

.text {
  transition: opacity 0.4s ease-in-out;
  font-size: 13px;
  letter-spacing: .1em;
}

.dash {
  transition: width 0.4s ease-in-out, opacity 0.4s ease-in-out;
  width: 32px;
  overflow: hidden;
  opacity: 0.6;
}

.link:hover .dash, .active .dash, 
.link:hover .text, .active .text {
  transition: all 0.2s ease-in-out;
  opacity: 1;
  filter: brightness(250%);
  font-weight: bold;
  width: 60px;
}

.active{
  font-weight: bold;
  filter: brightness(250%);
  margin:0;
}
</style>