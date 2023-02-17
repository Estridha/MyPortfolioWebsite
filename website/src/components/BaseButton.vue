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
  background-color: #4caf50; /* Green */
  border: none;
  border-radius: 8px;
  color: white;
  padding: 1rem;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;

  &:hover {
    cursor: pointer;
    opacity: 80%;
  }
}
</style>
