<template>
  <a href="#" v-if="windowTop > 400">
    <div class="arrow"></div>
  </a>
</template>
<script>
export default {
  data() {
    return {
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
  },
};
</script>
<style>
.arrow {
  width: 30px;
  height: 30px;
  text-align: center;
  border: solid var(--primary-color);
  border-width: 0 4px 4px 0;
  margin-left: 48%;
  transform: rotate(225deg);
  cursor: pointer;
  background-color: transparent !important;
  position: fixed;
  right: 20px;
  bottom: 20px;
}

.arrow:hover {
  border-color: purple;
  transition: 1s;
}
</style>
