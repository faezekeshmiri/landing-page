<template>
  <nav class="d-flex justify-space-between py-10">
    <div class="logo bg-red mx-5 px-1 py-1">logo</div>
    <div>
      <router-link class="mx-5" to="/">Day tours</router-link>
      <router-link class="mx-5" to="/">Multi-day tours</router-link>
      <router-link class="mx-5" to="/">Attractions</router-link>
      <router-link class="mx-5" to="/">Themes</router-link>
    </div>
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #2c3e50;
}

nav {
  
}

nav a {
  color: whitesmoke;
  text-decoration: none;
}

nav a.router-link-exact-active {
}
</style>
