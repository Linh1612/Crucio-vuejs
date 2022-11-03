<template>
  <div class="body-content7">
    <div
      :class="content7Item.className"
      v-for="content7Item in content7Items"
      :key="content7Item.id"
    >
      <div v-if="onShow() && show">
        <h3 :class="content7Item.count"></h3>
        <h4>{{ content7Item.paragraph }}</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      windowTop: 0,
      content7Items: [
        {
          id: 71,
          className: "parameter",
          count: "count1",
          paragraph: "Clients",
        },
        {
          id: 72,
          className: "parameter",
          count: "count2",
          paragraph: "Projects",
        },
        {
          id: 73,
          className: "parameter",
          count: "count3",
          paragraph: "Awards",
        },
        {
          id: 74,
          className: "parameter",
          count: "count4",
          paragraph: "Coffee",
        },
      ],
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
      if (this.windowTop > 3612) {
        this.show = true;
        return true;
      }
      return false;
    },
  },
};
</script>

<style scoped>
.body-content7 {
  height: 25rem;
  background-color: var(--primary-color);
  padding: 10rem;
  text-align: center;
  color: white;
  letter-spacing: 5px;
  font-size: 1.5rem;
  display: flex;
}

.body-content7 > .parameter {
  width: 25%;
}

.body-content7 > .parameter div h3 {
  padding-bottom: 2rem;
  font-size: 3rem;
  font-weight: 400;
}
</style>
