 <template>
      <main>
        <Header />
        <CVText />
      </main>

  </template>

  <script>

    import Header from "../components/Header.vue";
    import CVText from "../components/CVText.vue";
    export default {
      name: 'HomeView',
      components: { CVText, Header},
    };
  </script>
  <style lang="scss">
  </style>

