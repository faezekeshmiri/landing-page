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
  <v-container class="programs py-5">
    <v-row class="py-10" justify="center">
      <v-col cols="7">
        <div class="text-white py-5 text-h3 hero-title">Top Programs</div>
        <div class="text-white py-5 px-5 font-weight-thin">
          Our programs are compiled by the best guides. Each tourist will be
          able to choose a program according to their level.
        </div>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col
        cols="3"
        v-for="n in 3"
        :key="n"
        class="mx-2"
        :class="{
          'd-flex flex-column-reverse': n === 2,
          'd-flex flex-column': n != 2,
        }"
      >
        <v-row
          v-for="(program, index) in programs.slice(
            (n - 1) * 2,
            (n - 1) * 2 + 2
          )"
          :key="index"
          class="my-2"
        >
          <program-card
            :title="program.title"
            :cost="program.cost"
            :time="program.time"
            :image="program.image"
            :guide="program.guide"
            :profile="program.profile"
            :height="index % 2 === 0 ? 250 : 400"
          ></program-card>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ServiceCard from "@/components/ServiceCard.vue";
import ProgramCard from "@/components/ProgramCard.vue";
export default {
  name: "HomeView",
  components: {
    ServiceCard,
    ProgramCard,
  },
  data() {
    return {
      services: [
        {
          title: "Audio Guide",
          icon: "mdi-headset",
          description:
            "Travel on your own. Use the services of an audio guide.",
          link: "Select guide",
        },
        {
          title: "Programs",
          icon: "mdi-flag",
          description: "Choose a teravel program that is right for you.",
          link: "Select program",
        },
        {
          title: "Hotels & Restaurants",
          icon: "mdi-home",
          description: "Book hotels and restaurants at the best prices.",
          link: "learn more",
        },
      ],
      programs: [
        {
          title: "1The Best of Zurich",
          cost: "$80",
          time: "3 hours",
          image:
            "https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg",
          guide: "Tim hendricks",
          profile: "https://cdn.vuetifyjs.com/images/john.jpg",
        },
        {
          title: "2The Best of Zurich",
          cost: "$80",
          time: "3 hours",
          image:
            "https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg",
          guide: "Tim hendricks",
          profile: "https://cdn.vuetifyjs.com/images/john.jpg",
        },
        {
          title: "3The Best of Zurich",
          cost: "$80",
          time: "3 hours",
          image:
            "https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg",
          guide: "Tim hendricks",
          profile: "https://cdn.vuetifyjs.com/images/john.jpg",
        },
        {
          title: "4The Best of Zurich",
          cost: "$80",
          time: "3 hours",
          image:
            "https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg",
          guide: "Tim hendricks",
          profile: "https://cdn.vuetifyjs.com/images/john.jpg",
        },
        {
          title: "5The Best of Zurich",
          cost: "$80",
          time: "3 hours",
          image:
            "https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg",
          guide: "Tim hendricks",
          profile: "https://cdn.vuetifyjs.com/images/john.jpg",
        },
        {
          title: "6The Best of Zurich",
          cost: "$80",
          time: "3 hours",
          image:
            "https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg",
          guide: "Tim hendricks",
          profile: "https://cdn.vuetifyjs.com/images/john.jpg",
        },
      ],
    };
  },
};
</script>

<style>
.hero {
  /**background-size: cover;
  background-image: url(../assets/pexels-pixabay-355887.jpg);**/
}
.hero-des {
  width: 35%;
}
</style>
