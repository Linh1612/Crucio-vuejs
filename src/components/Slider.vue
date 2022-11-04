<!-- <template>
  <div class="carousel">
    <div class="carousel-inner">
      <carousel-items
        v-for="(slide, index) in slides"
        :slide="slide"
        :key="`item-${index}`"
        :current-slide="currentSlide"
        :index="index"
      ></carousel-items>
    </div>
  </div>
</template>
<script>
import CarouselItems from "./CarouselItems.vue";

export default {
  props: ["slides"],
  components: { CarouselItems },
  data() {
    return {
      currentSlide: 0,
      slideInterval: null,
    };
  },
  methods: {
    setCurrentSlide(index) {
      this.currentSlide = index;
    },
  },
  mounted() {
    this.slideInterval = setInterval(() => {
      const index =
        this.currentSlide < this.slides.length - 1 ? this.currentSlide + 1 : 0;
      this.setCurrentSlide(index);
    }, 3000);
  },
};
</script>

<style scoped>
.carousel {
  display: flex;
  justify-content: center;
}

.carousel-inner {
  position: relative;
  width: 900px;
  height: 400px;
  overflow: hidden;
}
</style> -->

<template>
  <carousel :items-to-show="1" :wrap-around="true" :autoplay="3000">
    <slide v-for="slide in 3" :key="slide">
      <div>
        <p>{{ content[slide - 1].value }}</p>
        <p>{{ content[slide - 1].name }}</p>
      </div>
      <!-- {{ slide }} -->
    </slide>

    <!-- <template #addons>
      <navigation />
      <pagination />
    </template> -->
  </carousel>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide } from "vue3-carousel";
//import { Navigation, Pagination } from "vue3-carousel";

export default {
  name: "App",
  components: {
    Carousel,
    Slide,
    // Pagination,
    // Navigation,
  },
  data() {
    return {
      content: [
        {
          value:
            "1Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
          name: "- Jim P. -",
        },
        {
          value:
            "2Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
          name: "- John K. -",
        },
        {
          value:
            "3Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
          name: "- Morgan F. -",
        },
      ],
    };
  },
};
</script>

<style scoped>
p {
  padding: 0 10rem;
  font-family: "Open Sans", sans-serif;
  color: rgb(222, 222, 222);
  line-height: 1.8;
  padding-bottom: 1rem;
  font-size: 1rem;
}
</style>
