<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { provide } from 'vue';

provide('perPage', 2);
</script>

<template>
  
  <div id="layout">
    <header>
      <div class="wrapper">
        <nav>
          <RouterLink to="/">Event</RouterLink> |
          <RouterLink to="/about">About</RouterLink> |
          <RouterLink to="/student">Student</RouterLink>
        </nav>
      </div>
    </header>
    
    <!-- <RouterView /> -->
  </div>
  <div id="app">
    <router-view :perPage="perPage"></router-view>
  </div>
</template>

<style>
#layout {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;


  text-align: center;
  margin-top: 2rem;
  color: #2c3e50;
}


  nav{
    padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  
}
nav a.router-link-exact-active {
  color: var(--color-text);
}
nav a.router-link-exact-active:hover {
  background-color: transparent;
}

  nav a.router-link-exact-active {
    color: #42b983;
}

h2 {
  font-size: 20px;
}
</style>
