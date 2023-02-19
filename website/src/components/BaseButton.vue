<template>
  <button :class="type" @click="$emit('userClicked')">{{ title }}</button>
</template>

<script>
export default {
  name: "BaseExperienceBlock",
  props: {
    type: String,
    title: String,
  },
};
</script>

<style scoped lang="scss">
button {
  font-size: 1rem;
  text-transform: uppercase;
  background-color: var(--button-color);
  border: none;
  border-radius: 8px;
  color: var(--light-color);
  padding: 1rem;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 1rem;
  min-width: 10rem;

  &:hover {
    cursor: pointer;
    opacity: 80%;
  }
}
</style>
