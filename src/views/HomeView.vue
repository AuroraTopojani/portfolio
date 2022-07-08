 <template>
      <main>
        <Header />
        <AboutMe />
        <CVText />
      </main>

  </template>

  <script>
    import AboutMe from "../components/AboutMe.vue";
    import Header from "../components/Header.vue";
    import CVText from "../components/CVText.vue";
    export default {
      name: 'HomeView',
      components: { CVText, Header, AboutMe },
    };
  </script>
  <style lang="scss">
  </style>

