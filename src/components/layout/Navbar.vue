<template>
  <main class="container">
    <div id="app">
    <section>
      <ul class="nav nav-tabs">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="/">Portfolio</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="">Works</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Contact</a>
        </li>

      </ul>
    </section>
    </div>


</main>
</template>


<div id="app">
<nav>
  <router-link to="/">Home</router-link> |
  <router-link to="/about">About</router-link>

</nav>
<router-view/>
</div>
<script>


export default {
  data(){
    return {
      count: 0
    }
  }
}
</script>

<style lang="scss">

</style>