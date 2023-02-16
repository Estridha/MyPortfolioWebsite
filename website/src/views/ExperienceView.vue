<template>
  <div class="experience">
    <BaseExperienceBlock
      type="work"
      title="Junior Full-Stack Software Developer"
      location="GetAccept"
      description="lorem ipsum"
    />
    <BaseExperienceBlock
      type="education"
      title="Bachelor of Science in Information Systems"
      location="Lund University of Economics and Management"
      description="lorem ipsum"
    />
    <BaseExperienceBlock
      type="education"
      title="Bachelor of Science in Information Systems"
      location="Lund University of Economics and Management"
      description="lorem ipsum"
    />
  </div>
</template>

<script>
import BaseExperienceBlock from "@/components/BaseExperienceBlock.vue";

export default {
  name: "ExperienceView",
  components: {
    BaseExperienceBlock,
  },
};
</script>

<style scoped lang="scss">
.block {
  border-radius: 2rem;
  background-color: #ffb703;
  display: flex;
  align-items: center;
  text-align: left;
  margin: 1rem;

  &.work {
    background: #219ebc;
  }
  img {
    max-width: 20%;
    padding: 1rem;
    height: fit-content;
    flex: 1;
  }
  .desc-container {
    flex: 2;
  }
}
</style>
