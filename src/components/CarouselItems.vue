<template>
  <transition name="slide-in">
    <div class="carousel-item" v-show="currentSlide === index">
      <p>{{ slide.value }}</p>
      <p>
        <i>{{ slide.name }}</i>
      </p>
    </div>
  </transition>
</template>

<script>
export default {
  props: ["slide", "currentSlide", "index"],
};
</script>

<style scoped>
.carousel-item {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

.slide-in-enter-active {
  transition: all 1s ease-in-out;
}

.slide-in-leave-active {
  transition: all 0s ease-in-out;
}

.slide-in-enter-from {
  transform: translateX(-100%);
}

.slide-in-leave-from {
  opacity: 0;
}
</style>
