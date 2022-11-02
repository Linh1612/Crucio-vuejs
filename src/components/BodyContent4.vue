<template>
  <div id="services" class="body-content4">
    <div class="text-center">
      <h2>SERVICES</h2>
      <hr />
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod
        tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea
        commodi consequat. Quis aute iure reprehenderit in voluptate velit esse
        cillum dolore eu fugiat nulla pariatur. Excepteur sint obcaecat
        cupiditat non proident, sunt in culpa qui officia deserunt mollit anim
        id est laborum.
      </p>
    </div>
    <div class="text-logo">
      <div
        :class="content4Item.father"
        v-for="content4Item in content4Items"
        :key="content4Item.id"
      >
        <div :class="content4Item.children">
          <iconify-icon :icon="content4Item.icon"></iconify-icon>
          <h4>{{ content4Item.headline }}</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content4Items: [
        {
          id: 41,
          father: "text",
          children: "logo",
          icon: "ion:desktop-outline",
          headline: "WEB DESIGN",
        },
        {
          id: 42,
          father: "text",
          children: "logo",
          icon: "ion:albums",
          headline: "BRAND DESIGN",
        },
        {
          id: 43,
          father: "text",
          children: "logo",
          icon: "eva:keypad-fill",
          headline: "UI/UX DESIGN",
        },
        {
          id: 44,
          father: "text",
          children: "logo",
          icon: "ion:color-palette",
          headline: "GRAPHIC DESIGN",
        },
        {
          id: 45,
          father: "text",
          children: "logo",
          icon: "ant-design:camera-filled",
          headline: "PHOTOGRAPHY",
        },
        {
          id: 46,
          father: "text",
          children: "logo",
          icon: "ic:baseline-videocam",
          headline: "VIDEO EDITING",
        },
        {
          id: 47,
          father: "text",
          children: "logo",
          icon: "ion:pulse",
          headline: "DATA ANALYSIS",
        },
        {
          id: 48,
          father: "text",
          children: "logo",
          icon: "bi:person-fill",
          headline: "CLIENT ASSISTANCE",
        },
      ],
    };
  },
};
</script>

<style scoped>
.body-content4 {
  height: 45rem;
}

.body-content4 > .text-center {
  padding-top: 15rem;
  text-align: center !important;
}

.body-content4 > .text-center h2 {
  letter-spacing: 5px;
  font-family: "Open Sans", sans-serif;
  font-size: 2rem;
  font-weight: 200;
  padding-bottom: 1rem;
}

.body-content4 > .text-center hr {
  width: 3rem;
  height: 3px;
  margin: 0 auto;
  background-color: rgb(173, 0, 255);
  border: none;
  margin-bottom: 2rem;
}

.body-content4 > .text-center p {
  color: var(--text-color);
  padding-left: 10rem;
  padding-right: 10rem;
  font-size: 14px;
  line-height: 1.8;
  letter-spacing: 1px;
  padding-bottom: 5rem;
}

.body-content4 > .text-logo {
  display: flex;
  flex-wrap: wrap;
  padding: 0 7rem;
  padding-left: 2rem;
}

.body-content4 > .text-logo > .text {
  width: 25%;
  padding-left: 5.5rem;
  display: inline-block;
  text-align: center;
}

.body-content4 > .text-logo > .text > .logo > iconify-icon {
  color: rgba(160, 32, 246, 1);
  font-size: 3rem;
  padding-top: 1rem;
  padding-left: 6rem;
}

.body-content4 > .text-logo > .text > .logo > iconify-icon:hover {
  color: #56007f;
  cursor: pointer;
  transition: 0.5s;
}

.body-content4 > .text-logo > .text > .logo > h4 {
  padding-top: 0.5rem;
  font-size: 1rem;
  letter-spacing: 1px;
  font-weight: 100;
  width: 15rem;
}
</style>
