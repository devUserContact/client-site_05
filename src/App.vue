<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home </RouterLink>
        <RouterLink to="/about">About </RouterLink>
      </nav>
    </div>
  </header>
  <body>
    <RouterView />
  </body>
</template>

<style scoped>
header {
  display: grid;
  height: 5%;
  border: solid;
}

nav {
  width: 100vh;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

@media (min-width: 1024px) {
  header .wrapper {
    display: grid;
  }

  nav {
    text-align: left;
    font-size: 1rem;
    margin-top: 1rem;
  }
}
</style>
