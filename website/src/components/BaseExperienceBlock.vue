<template>
  <div :class="type" class="wrapper">
    <img v-if="type === 'work'" src="@/assets/icons/work.svg" alt="" />
    <img
      v-if="type === 'education'"
      src="@/assets/icons/university.svg"
      alt=""
    />
    <div class="desc-container">
      <h3>{{ title }}</h3>
      <h4>{{ location }}</h4>
      <p>{{ description }}</p>
    </div>
  </div>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: "BaseExperienceBlock",
  props: {
    logoSrc: String,
    type: String,
    title: String,
    location: String,
    description: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.wrapper {
  border-radius: 2rem;
  background-color: #ffb703;
  display: flex;
  align-items: center;
  text-align: left;
  margin: 1rem;
  padding: 1rem;

  &.work {
    background-color: #219ebc;
  }
  img {
    padding-right: 2rem;
    max-width: 20%;
    height: fit-content;
    flex: 1;

    @media only screen and (max-width: 450px) {
      display: none;
    }
  }
  .desc-container {
    flex: 2;
  }
}
</style>
