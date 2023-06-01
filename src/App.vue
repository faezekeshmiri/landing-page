<template>
  <nav class="d-flex justify-space-between py-1">
    <div class="logo bg-red-darken-1 mx-5 px-1 py-1">logo</div>
    <div>
      <router-link class="mx-5" to="/">Day tours</router-link>
      <router-link class="mx-5" to="/">Multi-day tours</router-link>
      <router-link class="mx-5" to="/">Attractions</router-link>
      <router-link class="mx-5" to="/">Themes</router-link>
      <span class="bg-red-darken-1 py-5 px-2">
        <v-btn variant="text" icon="mdi-menu" class="text-white" @click.stop="drawer = !drawer"></v-btn>
      </span>
    </div>
  </nav>
  <v-layout>
    <v-navigation-drawer
        v-model="drawer"
        location="right"
        temporary
        class="bg-purple-darken-4"
      >
      <v-list>
        <v-list-group v-for="(item, index) in items" :key="index"  :value="item.title">
          <template v-slot:activator="{ props }">
            <v-list-item
              dir="rtl"
              v-bind="props"
              :prepend-icon="item.icon"
              :title="item.title"
            ></v-list-item>
          </template>
          <v-list-item
              v-for="(subitem, i) in item.subItems"
              :key="i"
              :title="subitem.title"
              :prepend-icon="subitem.icon"
              :value="title"
              dir="rtl"
            ></v-list-item>
        </v-list-group>
      </v-list>
      </v-navigation-drawer>
  </v-layout>
  <div>
    <router-view/>
  </div>
</template>

<script>
  export default {
    data: () => ({
      drawer: false,
      group: null,
      items: [
        {title: 'projects', icon: 'mdi-folder' , subItems: [
          {title: 'project1', icon: 'mdi-file'},
          {title: 'project2', icon: 'mdi-file'},
          {title: 'project3', icon: 'mdi-file'}
        ]}
      ]
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #080e21;
  padding: 0px;
  margin: 0px;
  background-size: 100% 50%;
  background-image: url(./assets/bg.png);
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
