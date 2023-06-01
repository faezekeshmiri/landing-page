<template>
  <v-container class="hero py-5">
    <v-row class="py-10" justify="center">
      <v-col cols="7">
        <div class="text-white py-5 text-h2 hero-title">
          Switzerland Has Never Been So Affordable
        </div>
        <div class="text-white py-5 px-5 font-weight-thin">
          Discover Switzerland. Choose the best program, guides, hotels and
          restaurants.
        </div>
        <div class="py-5">
          <v-btn class="bg-red-darken-1 px-5" height="50px"
            >Start to explore</v-btn
          >
        </div>
      </v-col>
    </v-row>
    <v-row>
      <service-card
        class="mx-2"
        v-for="service in services"
        :key="service.title"
        :title="service.title"
        :icon="service.icon"
      ></service-card>
    </v-row>
  </v-container>
</template>

<script>
import ServiceCard from "@/components/ServiceCard.vue";
export default {
  name: "HomeView",
  components: {
    ServiceCard,
  },
  data() {
    return {
      services: [
        { title: "Audio Guid", icon: "mdi-music" },
        { title: "Programs" },
        { title: "Hotels & Restaurants", icon: "mdi-home" },
      ],
    };
  },
};
</script>

<style>
.hero{
  /**background-size: cover;
  background-image: url(../assets/pexels-pixabay-355887.jpg);**/
}
.hero-des {
  width: 40%;
}
</style>
