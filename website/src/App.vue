<template>
  <div class="wrapper" :style="{ height: windowHeight.toString() + 'px' }">
    <AppHeader />
    <div class="content-container">
      <router-view />
      <AppFooter />
    </div>
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
import AppFooter from "@/components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppFooter,
  },
  data() {
    return {
      windowHeight: window.innerHeight,
    };
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener("resize", this.onResize);
    });
  },
  beforeUnmount() {
    window.removeEventListener("resize", this.onResize);
  },
  methods: {
    onResize() {
      this.windowHeight = window.innerHeight;
    },
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap');
@import './assets/styles/variables.css';

* {
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
  list-style: none;
  text-decoration: none;
}
html,
body {
  margin: 0;
  background-color: var(--light-color);
  color: var(--dark-color);
  h1,
  h2,
  h3 {
    font-weight: 800;
  }
  h4 {
    font-weight: 600;
  }
  p,
  a,
  label, button {
    font-weight: 400;
  }
  a {
    color: var(--link-color);
  }
}

#app {
  margin: 0;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  overflow: none;
}

.content-container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 85%;
  overflow-y: scroll;
}

.wrapper {
  overflow: none;
}
</style>
