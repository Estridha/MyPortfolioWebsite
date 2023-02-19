<template>
  <div class="wrapper">
    <div class="message-container">
      <h3>Message was sent!</h3>
      <p>
        Your message was sent successfully, I will get back to you as fast as I
        can!
      </p>
    </div>
    <BaseButton title="Go Back" @userClicked="$router.push('/contact')" />
  </div>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";

export default {
  name: "ContactView",
  components: { BaseButton },
};
</script>

<style scoped lang="scss">
.wrapper {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  height: 80%;

  .message-container {
    margin: 2rem;
    padding: 1rem;
    background: var(--dark-color);
    color: var(--light-color);
    border-radius: 8px;

    p {
      margin: 2rem;
    }

    h3 {
      @media only screen and (max-width: 740px) {
        display: none;
      }
    }
  }
}
</style>
