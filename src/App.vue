<template>
  <nav class="d-flex justify-space-between py-1">
    <div class="logo bg-red-darken-1 mx-5 px-1 py-1">logo</div>
    <div>
      <router-link class="mx-5" to="/">Day tours</router-link>
      <router-link class="mx-5" to="/">Multi-day tours</router-link>
      <router-link class="mx-5" to="/">Attractions</router-link>
      <router-link class="mx-5" to="/">Themes</router-link>
      <span class="bg-red-darken-1 py-5 px-2">
        <v-btn variant="text" icon="mdi-menu" class="text-white"></v-btn>
      </span>
    </div>
  </nav>
  <div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #2c3e50;
  padding: 0px;
  margin: 0px;
}

nav {
  border-bottom: 1px solid #CFD8DC;
}

nav a {
  color: whitesmoke;
  text-decoration: none;
}

nav a.router-link-exact-active {
}
</style>
