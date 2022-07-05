<template>
  <div id="app">
    <main>
      <Navbar/>
      <CVText/>
    </main>
  </div>
</template>

<script>
import Navbar from "./components/layout/Navbar.vue";
import CVText from "@/components/CVText.vue";
export default {
  name:'',
  components: {CVText, Navbar}
}
</script>
<style lang="scss">

</style>