<template>
  <div class="wrapper">
    <BaseProjectBlock
      customer="Kevan Doyle"
      title="Videographer Portfolio Website"
      date="2022"
      filename="kevan-doyle.png"
      description="Built a portfolio website for a photographer/videographer as a freelance project. Got familiar with using netlify for hosting."
      :technologies="['JavaScript', 'Vue.js', 'HTML5', 'SaSS']"
      :links="[
        { name: 'Visit Website', href: 'http://kevandoyle.netlify.app' },
        { name: 'Code on Github', href: 'https://github.com/Estridha/kevan-doyle' },
      ]"
    />
  </div>
</template>

<script>
import BaseProjectBlock from "@/components/BaseProjectBlock.vue";

export default {
  name: "ProjectsView",
  components: { BaseProjectBlock },
};
</script>
