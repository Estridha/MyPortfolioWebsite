<template>
  <div class="title-container">
    <h3>{{ title }}</h3>
  </div>
</template>

<script>
export default {
  name: "BaseH3",
  props: {
    title: String,
  },
};
</script>

<style scoped lang="scss">
.title-container {
    border-left: solid 2px;
    margin: 2rem;
    text-align: left;
    h3 {
    text-transform: uppercase;
    margin-left: 1rem;
    }
}
</style>
