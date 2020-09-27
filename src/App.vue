<template>
  <Header />
  <HeroArea />
  <About />
  <Contact />
</template>

<script>
import HeroArea from "./components/HeroArea.vue";
import About from "./components/About.vue";
import Contact from "./components/Contact.vue";

import Header from "./components/Header";

export default {
  name: "App",
  components: {
    HeroArea,
    About,
    Contact,
    Header,
  },
};
</script>

<style>
html {
  scroll-behavior: smooth;
}
#app {
  font-family: "Nunito Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.full-vp {
  width: 100vw;
  height: 100vh;
  max-width: 100%;
}

.inner {
  max-width: 1200px;
  margin: 0 auto;
  padding-top: 70px;
}
</style>
