<template>
  <div :class="type" class="wrapper">
    <div class="desc-container">
      <h4>{{ location }}</h4>
      <h3>{{ title }}</h3>
      <p class="date">{{ date }}</p>
      <p>{{ description }}</p>
    </div>
    <img v-if="type === 'work'" src="@/assets/icons/work.svg" alt="" />
    <img
      v-if="type === 'education'"
      src="@/assets/icons/university.svg"
      alt=""
    />
  </div>
</template>

<script>
export default {
  name: "BaseExperienceBlock",
  props: {
    date: String,
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
  background-color: var(--dark-color);
  color: var(--light-color);
  display: flex;
  align-items: center;
  text-align: left;
  margin: 1rem 2rem;
  padding: 1rem 3rem;

  @media only screen and (max-width: 450px) {
    padding: 1rem;
  }
  img {
    padding-left: 2rem;
    max-width: 20%;
    height: fit-content;
    flex: 1;

    @media only screen and (max-width: 450px) {
        display: none;
    }
  }
  .desc-container {
    flex: 2;

    .date {
      border-radius: 8px;
      margin: 0;
    }

    h3 {
      margin: 0;
    }

    h4 {
      margin-bottom: 0.5rem;
    }
  }
}
</style>
