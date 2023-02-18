<template>
  <div class="wrapper">
    <div class="desc-container">
      <div class="project-container">
        <h4>{{ date }}</h4>
        <h3>{{ title }}</h3>
        <div class="link-container">
          <a v-for="link in links" :key="link.index" :href="link.href">{{
            link.name
          }}</a>
        </div>
        <p>{{ description }}</p>
      </div>
      <div class="technologies-container">
        <h4>Technologies</h4>
        <div class="technology-block-container">
          <p
            class="technology-block"
            v-for="technology in technologies"
            :key="technology.index"
          >
            {{ technology }}
          </p>
        </div>
      </div>
    </div>
    <img :src="require(`@/assets/images/projects/${filename}`)" alt="" />
  </div>
</template>

<script>
export default {
  name: "BaseProjectBlock",
  props: {
    date: String,
    title: String,
    description: String,
    links: Array,
    technologies: Array,
    filename: String,
  },
};
</script>

<style scoped lang="scss">
.wrapper {
  background-color: #219ebc;
  border-radius: 2rem;
  display: flex;
  text-align: left;
  margin: 1rem 2rem;
  padding: 1rem 3rem;

  @media only screen and (max-width: 740px) {
    padding: 1rem;
    flex-direction: column-reverse;
  }

  .desc-container {
    flex: 1;
    max-width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    .project-container {
      .link-container {
        display: inline-flex;
        align-items: center;
        margin-top: 0.5rem;

        & > a {
          padding-right: 0.5rem;
          &:not(:first-child) {
            padding-left: 0.5rem;
            border-left: solid black 1px;
          }
        }

        .divider {
          margin: 0 0.5rem;
        }
      }
    }

    h3 {
      margin: 0;
    }

    h4 {
      margin-bottom: 0.5rem;
    }
    .technology-block-container {
      display: flex;
      flex-wrap: wrap;

      @media only screen and (max-width: 740px) {
        justify-content: space-between;
      }
      .technology-block {
        padding: 1rem;
        border-radius: 8px;
        margin: 0 1rem 1rem 0;
        background-color: aquamarine;
        @media only screen and (max-width: 740px) {
          margin: 0 0 1rem 0;
          width: 47%;
          text-align: center;
        }
      }
    }
  }

  img {
    border-radius: 1rem;
    align-self: center;
    width: 50%;
    flex: 1;
    margin-left: 1rem;

    @media only screen and (max-width: 740px) {
      width: 100%;
      margin-right: 1rem;
    }
  }
}
</style>
