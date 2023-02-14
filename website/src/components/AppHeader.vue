<template>
  <nav>
    <router-link to="/">Home</router-link>
    <router-link to="/experience">Experience</router-link>
    <router-link to="/projects">Projects</router-link>
    <router-link to="/contact">Contact</router-link>
  </nav>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
nav {
  display: flex;
  position: sticky;
  top: 0;
  justify-content: center;
  width: 100%;
  padding: 30px;

  a {
    padding: 0 2rem;
    font-weight: bold;
    color: #000000;
    text-decoration: none;

    &.router-link-exact-active {
      color: #ffa321;
    }
  }
}
</style>
