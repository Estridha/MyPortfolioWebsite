<template>
  <div class="wrapper" :style="{height: (windowHeight.toString() + 'px')}">
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
  data() {
    return {
      windowHeight: window.innerHeight
    }
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener('resize', this.onResize);
    })
  },
  beforeUnmount() { 
    window.removeEventListener('resize', this.onResize); 
  },
  methods: {  
    onResize() {
      this.windowHeight = window.innerHeight
    }
  }
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
  list-style: none;
  text-decoration: none;
}
html,
body {
  margin: 0;
}

#app {
  margin: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.wrapper {
  height: v-bind(windowHeight);
  display: flex;
  justify-content: space-between;
  flex-direction: column;
}
</style>
