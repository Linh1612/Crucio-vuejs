<template>
  <div class="body-content11">
    <div class="text-center">
      <h3>TESTIMONIALS</h3>
      <hr />
      <!-- <p>
        Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod
        tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea
        commodi consequat. Quis aute iure reprehenderit in voluptate velit esse
        cillum dolore eu fugiat nulla pariatur.
      </p>
      <p><i>-Jim P.-</i></p> -->
      <div
        :class="content11Item.className"
        v-for="content11Item in content11Items"
        :key="content11Item.id"
        @click="checkClass"
      >
        <p>
          {{ content11Item.value }}
        </p>
        <p>
          <i>{{ content11Items.name }}</i>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content11Items: [
        {
          id: 0,
          value:
            "Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
          name: "- Jim P. -",
          className: "visible",
        },
        {
          id: 1,
          value:
            "Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
          name: "- John K. -",
          className: "hidden",
        },
        {
          id: 2,
          value:
            "Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
          name: "- Morgan F. -",
          className: "hidden",
        },
      ],
    };
  },
  methods: {},
};
</script>

<style scoped>
.body-content11 {
  height: 30rem;
  background-color: rgb(11, 11, 11);
}

.body-content11 > .text-center {
  color: white;
  text-align: center !important;
  padding: 7rem;
}

.body-content11 > .text-center h3 {
  letter-spacing: 3px;
  font-family: "Open Sans", sans-serif;
  text-transform: uppercase;
  font-size: 2rem;
  font-weight: 400;
  padding-bottom: 2rem;
}

.body-content11 > .text-center hr {
  width: 3rem;
  height: 3px;
  margin: 0 auto;
  background-color: white;
  border: none;
  margin-bottom: 2rem;
}

.body-content11 > .text-center > div > p {
  padding: 0 10rem;
  font-family: "Open Sans", sans-serif;
  color: rgb(222, 222, 222);
  line-height: 1.8;
  padding-bottom: 1rem;
  font-size: 1rem;
}

.body-content11 > .text-center > .hidden {
  opacity: 0;
}

.body-content11 > .text-center > .visible {
  opacity: 1;
}
</style>
