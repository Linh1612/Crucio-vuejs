<template>
  <header-app />
  <body-app />
  <footer-app />
</template>

<script>
import Header from "./components/Header.vue";
import Body from "./components/Body.vue";
import "animate.css";
import "./assets/styles/global.css";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    HeaderApp: Header,
    BodyApp: Body,
    FooterApp: Footer,
  },
};
</script>
