<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import MyCounter from './components/MyCounter.vue'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/ex1">ex1</RouterLink>
      <RouterLink to="/ex2">ex2</RouterLink>
      <RouterLink to="/ex3">ex3</RouterLink>
      <RouterLink to="/ex4">ex4</RouterLink>
      <RouterLink to="/ex5">ex5</RouterLink>
      <RouterLink to="/ex6">ex6</RouterLink>
      <RouterLink to="/ex7">ex7</RouterLink>
      <RouterLink to="/ex8">ex8</RouterLink>
      <RouterLink to="/ex9">ex9</RouterLink>
      <RouterLink to="/ex10">ex10</RouterLink>
      <RouterLink to="/ex11">ex11</RouterLink>
      <RouterLink to="/ex12">ex12</RouterLink>
      <RouterLink to="/sandbox">sandbox</RouterLink>
      <RouterLink to="/cycle">CYCLE DE VIE</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
