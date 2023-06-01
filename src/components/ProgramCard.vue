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
        guide: String,
        profile: String,
        height: Number
    }
}
</script>