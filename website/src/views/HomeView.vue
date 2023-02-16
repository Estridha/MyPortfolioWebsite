<template>
  <div class="wrapper">
    <h1 class="title">Hi, I'm Estrid</h1>
    <p>I am an information system student and full-stack developer. Welcome to my website!</p>
    <div class="button-container">
    <button>Projects</button>
    <button>Experience</button>
  </div>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
}
</script>

<style scoped lang="scss">
.wrapper {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: 0 2rem;
}

.button-container {
  display: flex;
  justify-content: center;

  button {
    margin: 2rem;
  }
}

</style>