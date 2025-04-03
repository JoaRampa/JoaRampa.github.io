<script>
  import About from './components/about.vue';
  import Title from './components/title.vue';
  import Nav from './components/nav.vue';
  import SocialMedia from './components/socialMedia.vue';

  export default {
    components: {Title, About, Nav, SocialMedia},
    data() {
      return {
        showNav: window.innerWidth > 1000
      };
    },
    methods: {
      checkWidth() {
        this.showNav = window.innerWidth > 1000;
      }
    },
    mounted() {
      window.addEventListener('resize', this.checkWidth);
    },
  }
</script>

<template>
  <div class="container">
      <div class="title">
        <Title />
        <Nav v-if="showNav"/>
        <SocialMedia />
      </div>
    <div class="content">
      <h1 v-if="!showNav">About</h1>
      <About />
    </div>
  </div>
</template>

<style>
  html, body, #app {
    margin: 0;
    background-color: #0a192f;
    color: rgb(226 232 240);
    scroll-behavior: smooth;
    font-family: sans-serif;
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
      justify-content: left;
      padding-left: 0;
    }

    .content {
      padding-right: 0;
      margin-left: 0;
      width: 100%;
    }

    .social-links {
      margin-top: 2rem;
    }
  }
</style>
