<script>
  import About from './components/about.vue';
  import Title from './components/title.vue';
  import Nav from './components/nav.vue';
  import SocialMedia from './components/socialMedia.vue';
  import Projects from './components/projects.vue';

  export default {
    components: {Title, About, Nav, SocialMedia, Projects},
    data() {
      return {
        showNav: window.innerWidth > 1000
      };
    },
    methods: {
      checkWidth() {
        this.showNav = window.innerWidth > 1000;
      },

      light(event) { 
        const mouseX = `${event.clientX}px`;
        const mouseY = `${event.clientY}px`;

        document.documentElement.style.setProperty('--mouse-x', mouseX);
        document.documentElement.style.setProperty('--mouse-y', mouseY);
      },
    },
    mounted() {
      window.addEventListener('resize', this.checkWidth);
      window.addEventListener('mousemove',this.light)
    },
    beforeUnmount() {
      window.removeEventListener('resize', this.checkWidth);
      window.removeEventListener('mousemove', this.light);
    }
  }
</script>

<template>
  <div class="efectoLinterna"></div>
    <div class="container">
        <div class="title">
          <Title />
          <Nav v-if="showNav"/>
          <SocialMedia />
        </div>
      <div class="content">
        <section id="about">
          <h3 v-if="!showNav">ABOUT</h3>
          <About />
        </section>
        <section id="projects">
          <h3 v-if="!showNav">PROJECTS</h3>
          <Projects />
        </section>
      </div>
    </div>
</template>

<style>
  html, body, #app {
    margin: 0;
    overflow-x: hidden;
    background-color: #03132d;
    color: rgb(226 232 240);
    scroll-behavior: smooth;
    font-family: sans-serif;
  }

  :root {
    --mouse-x: 50vw;
    --mouse-y: 50vh;
  }

  h3 {
    font-weight: 700;
    letter-spacing: .1em;
  }

  .efectoLinterna {
    position: fixed;
    pointer-events: none;
    width: 100%;
    height: 100%;
    z-index: 9999;
    background: radial-gradient(circle 250px at var(--mouse-x) var(--mouse-y), rgba(255, 255, 255, 0.15), transparent);
  }

  .container {
    display: flex;
    justify-content: space-between;
    align-items: flex-start; 
    padding: 5rem 0;
  }

  .title {
    position: fixed;  
    display: grid;
    height: 50vh;
    grid-template-columns: 1fr;
    width: 50%;
    padding-left: 9rem;
  }

  .content {
    display: grid;
    row-gap: 6rem;
    box-sizing: border-box;
    margin-left: 50%;
    padding-right: 9rem;
  }

  @media (max-width: 1000px) {

    .container {
      display: block;
      padding: 5rem;
    }

    .title {
      position: relative;
      height: auto;
      padding-left: 0;
      min-width: 350px;
      margin-bottom: 3rem;
    }

    .content {
      padding-right: 0;
      margin-left: 0;
      width: 100%;
      row-gap: 3rem;
    }

    .social-links {
      margin-top: 2rem;
    }
  }
</style>
