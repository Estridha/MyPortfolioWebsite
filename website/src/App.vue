<template>
  <div class="wrapper">
  <AppHeader />
  <router-view />
  <AppFooter />
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
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
  list-style: none;
  text-decoration: none;
}

html, body {
  margin: 0;
  height: 100%;
}

#app {
  margin: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}

.wrapper {
  height: 100%;
  display: flex;
  justify-content: space-between;
  flex-direction: column;
}
</style>
