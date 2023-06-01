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
    <v-row justify="center">
      <service-card
        class="mx-2"
        v-for="service in services"
        :key="service.title"
        :title="service.title"
        :icon="service.icon"
        :description="service.description"
        :link="service.link"
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
        { title: "Audio Guide", icon: "mdi-headset", description:'Travel on your own. Use the services of an audio guide.', link: 'Select guide' },
        { title: "Programs", icon: "mdi-flag", description:'Choose a teravel program that is right for you.', link: 'Select program' },
        { title: "Hotels & Restaurants", icon: "mdi-home", description:'Book hotels and restaurants at the best prices.',link: 'learn more' },
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
