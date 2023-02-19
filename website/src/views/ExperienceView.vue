<template>
  <div class="wrapper">
    <div class="desc-container">
      <p>
        I’ve always sought out challenges and opportunities that are meaningful
        to me. Although my professional path has taken many twists and turns —
        from touring flow artist, to employee at a large company, to being an
        active member of my student union and freelancing as a web developer to
        build websites for my friends — I've never stopped engaging my passion
        to help others and solve problems. <br />
        <br />
        As a developer, I enjoy using my obsessive attention to detail, my
        unequivocal love for building things, and my mission-driven work ethic
        to make important change. I'm currently finishing my last term at the
        Bachelor’s Programme in Information Systems at Lund University and am on
        the lookout for an exiting opportunity that’ll kickstart my career in
        Software Development. <br />
        <br />I'm an optimistic person who is passionate about code and enjoys
        coming up with solutions to difficult problems and am eager to make a
        big impact at a high growth company.
      </p>
      <img src="@/assets/profile-picture.jpg" alt="" />
    </div>
    <BaseH3 title="Previous roles" />
    <BaseExperienceBlock
      type="work"
      title="Junior Full-Stack Software Developer"
      location="GetAccept"
      date="April 2020 - September 2022"
      description="Worked with developing and maintaining the digital sales room platform along with experienced developers and designers. Solved bugs, developed new functions and wrote unit tests. Participated in daily meetings and code reviews. Became familiar with web development and modern technologies such as Vue.js, TypeScript, SaSS and GraphQL."
    />
    <BaseExperienceBlock
      type="work"
      title="Corporate Relations Coordinator"
      location="LundaEkonomerna"
      date="September 2020 - April 2021"
      description="Responsible for managing and acquiring companies to participate in Samday 2020, the largest career fair for the informatics students at Lund University."
    />
    <BaseH3 title="Education" />
    <BaseExperienceBlock
      type="education"
      title="Bachelor of Science in Information Systems"
      location="Lund University of Economics and Management"
      date="August 2019 - Present"
    />
    <BaseExperienceBlock
      type="education"
      title="Education Abroad Programme with focus on Technology Management"
      location="University of California Santa Barbara"
      date="August 2021 - June 2022"
      description="Participated in the Education Abroad Program on a full scholarship."
    />
    <BaseExperienceBlock
      type="education"
      title="Graphic Design"
      location="Malmö University"
      date="January 2019 - June 2019"
    />
  </div>
</template>

<script>
import BaseExperienceBlock from "@/components/BaseExperienceBlock.vue";
import BaseH3 from "@/components/BaseH3.vue";

export default {
  name: "ExperienceView",
  components: {
    BaseExperienceBlock,
    BaseH3,
  },
};
</script>

<style scoped lang="scss">
.wrapper {
  .desc-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    text-align: left;
    margin: 0 2rem;
    img {
      border-radius: 50%;
      height: 10rem;
      width: fit-content;
      margin-left: 2rem;
      @media only screen and (max-width: 740px) {
        display: none;
      }
    }
  }
}
</style>
