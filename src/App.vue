<script>
  import About from './components/about.vue';
  import Title from './components/title.vue';
  import Nav from './components/nav.vue';

  export default {
    components: {Title, About, Nav},
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
    padding: 0;
    height: 100%;
    background-color: #0a192f;
    color: rgb(226 232 240);
    scroll-behavior: smooth;
    font-family: 'Inter', sans-serif;
  }

  .container {
    height: 100vh;
    padding: 1rem;
  }

  .title {
    position: fixed;  
    height: 100vh;
    width: 100%;
    padding: 20px;
  }

  .content {
    margin-left: 50%;
    height: 100vh;
    padding: 20px;
    box-sizing: border-box;
  }

  @media (max-width: 1000px) {
    .title {
      position: relative;
      width: 100%;
      height: auto;
      justify-content: left;
    }

    .content {
      margin-left: 0;
      width: 100%;
    }
  }
</style>
