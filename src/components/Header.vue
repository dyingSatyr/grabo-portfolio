<template>
  <div class="header">
    <div class="inner">
      <a href="#hero-area" @click="smoothScrollTo($event)">
        <img alt="Boris Grabovac" src="../assets/logo.png" />
      </a>
      <nav>
        <a href="#about" @click="smoothScrollTo($event)">About</a>
        <a href="#contact" @click="smoothScrollTo($event)">Contact</a>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  methods: {
    smoothScrollTo(e) {
      e.preventDefault();
      let id = "";
      //If img clicked, get id from parent A tag, or directly from link
      e.target.hash ? (id = e.target.hash) : (id = e.target.parentElement.hash);

      document.querySelector(id).scrollIntoView({
        block: "start",
        behavior: "smooth",
      });
    },
  },
};
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  width: 100%;
  background: rgba(0, 0, 0, 0.1);
}

.inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
}

nav a {
  text-decoration: none;
  color: #fff;
  margin-left: 30px;
  transition: all 0.3s;
}

nav a:hover {
  opacity: 0.8;
}
</style>
