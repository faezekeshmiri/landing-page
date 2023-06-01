<template>
    <v-card>
        <v-img
          width="300"
          :height="height"
          :src="image"
          cover
          class="text-white"
        >
          <v-card-title class="text-left">{{ title }}</v-card-title>
          <v-card-subtitle class="d-flex text-white justify-start">
            <span>
              <v-icon icon="mdi-label"></v-icon>
              {{ cost }}
            </span>
            <span class="ml-3">
              <v-icon icon="mdi-clock"></v-icon>
              {{ time }}</span
            >
          </v-card-subtitle>
          <v-card-actions class="profile">
            <v-list-item>
              <template v-slot:prepend>
                <v-avatar
                  class="elevation-15"
                  :image="profile"
                ></v-avatar>
              </template>
      
              <v-list-item-title>{{name}}</v-list-item-title>
      
              <v-list-item-subtitle>{{role}}</v-list-item-subtitle>
            </v-list-item>
          </v-card-actions>
        </v-img>
      </v-card>
</template>

<script>
export default{
    name: 'ProgramCard',
    props: {
        title: String,
        cost: String,
        time: String,
        image: String,
        name: String,
        role:String,
        profile: String,
        height: Number
    }
}
</script>

<style>
.profile {
    position: absolute;
    bottom: 0;
}
</style>