<template>
  <div class="body-content3">
    <div
      :class="content3Item.className"
      v-for="content3Item in content3Items"
      :key="content3Item.id"
    >
      <h3>{{ content3Item.headline }}</h3>
      <p>{{ content3Item.paragraph }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content3Items: [
        {
          id: 31,
          className: "row bgcolor1",
          background: "#AD00FF",
          headline: "RESPONSIVE",
          paragraph:
            "Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat.",
        },
        {
          id: 32,
          className: "row bgcolor2",
          background: "#8200BF",
          headline: "CUSTOMIZABLE",
          paragraph:
            "Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat.",
        },
        {
          id: 33,
          className: "row bgcolor3",
          background: "#56007F",
          headline: "MODERN",
          paragraph:
            "Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.body-content3 {
  display: flex;
  height: 20rem;
}

.body-content3 > .row {
  width: 33.3%;
  padding: 5rem;
  color: #fff;
}

.body-content3 div h3 {
  letter-spacing: 1px;
  padding-bottom: 2.5rem;
  font-size: 2rem;
}

.body-content3 > .bgcolor1 {
  background-color: #ad00ff;
}

.body-content3 > .bgcolor2 {
  background-color: #8200bf;
}

.body-content3 > .bgcolor3 {
  background-color: #56007f;
}
</style>
