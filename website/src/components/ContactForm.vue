<template>
  <div class="desc-container">
    <p>If you want to get in touch with me feel free to
    <a href="https://www.linkedin.com/in/estridhassbring/">send me a message on linkedin</a>,
    or simply use the contact form below.</p>
  </div>
  <div class="main-container">
    <form
      class="form-group"
      action="https://formsubmit.co/6b09b0cefdfd08ac5ba34b5da89d946c"
      method="POST"
    >
      <!-- Honeypot -->
      <input type="text" name="_honey" style="display: none" />
      <!-- Disable Captcha -->
      <input type="hidden" name="_captcha" value="false" />
      <input
        type="hidden"
        name="_next"
        value="http://localhost:8080/contact/success"
      />
      <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" name="Name" required />
      </div>
      <div class="form-group">
        <label for="email">E-mail:</label>
        <input type="email" name="E-mail" required />
      </div>
      <div class="form-group">
        <label for="message">Message:</label>
        <textarea name="Message" rows="10" required></textarea>
      </div>
      <div class="button-container">
        <BaseButton type="primary" title="Send" />
      </div>
    </form>
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";
export default {
  name: "ContactForm",
  components: {
    BaseButton,
  },
  methods: {
    sayHello() {
      console.log("hello");
    },
  },
};
</script>

<style lang="scss" scoped>
.title {
  @media only screen and (max-width: 450px) {
    display: none;
  }
}

.desc-container {
  display: flex;
  padding: 0 2rem;
  text-align: left;
}
.main-container {
  padding: 1rem;
  border-radius: 8px;
  margin: 2rem;
  background-color: var(--dark-color);
  color: var(--light-color);

  .form-group {
    margin-top: 1rem;
    font-size: 1rem;
    input {
      height: 2rem;
      &:focus-visible {
        outline: var(--light-color) auto 1px;
      }
    }
    textarea {
      height: 15rem;
      &:focus-visible {
        outline: var(--light-color) auto 1px;
      }
    }
  }
  .form-group input,
  .form-group textarea {
    width: 100%;
    border: 1px solid rgba(128, 128, 128, 0.199);
    margin-top: 0.5rem;
  }
  textarea {
    resize: vertical;
  }

  .button-container {
    margin-top: 1rem;
  }
}
</style>
