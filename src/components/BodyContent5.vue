<template>
  <div class="body-content5">
    <div class="title-btn" v-if="onShow() && show">
      <h2 class="leftToCenter">WE CREATE <strong>AWESOME</strong> PROJECTS</h2>
      <button class="bottomToTop">GET STARTED</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      windowTop: 0,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll(e) {
      this.windowTop = e.target.documentElement.scrollTop;
    },
    onShow() {
      if (this.show) return true;
      if (this.windowTop > 2250) {
        this.show = true;
        return true;
      }
      return false;
    },
  },
};
</script>

<style scoped>
.body-content5 {
  height: 25rem;
  background-color: var(--primary-color);
  margin-top: 10rem;
  padding: 10rem;
  text-align: center;
  color: white;
  letter-spacing: 10px;
  font-size: 1.5rem;
}

.body-content5 > .title-btn h2 {
  font-weight: 100;
  padding-bottom: 3rem;
}

.body-content5 > .title-btn button {
  width: 12.5rem;
  height: 3rem;
  background-color: var(--primary-color);
  border: 3px solid white;
  color: white;
  font-size: 1rem;
  letter-spacing: 2px;
  cursor: pointer;
}

.body-content5 > .title-btn button:hover {
  background-color: white;
  color: var(--primary-color);
  transition: 1s;
}
</style>
