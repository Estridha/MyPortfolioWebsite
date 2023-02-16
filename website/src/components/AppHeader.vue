<template>
  <nav>
    <div v-if="!menuIsOpen" class="nav-container">
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/experience">Experience</router-link></li>
      <li><router-link to="/projects">Projects</router-link></li>
      <li><router-link to="/contact">Contact</router-link></li>
    </div>
    <div class="mobile-nav-container">
      <button class="mobile-button" @click="toggleMenu"></button>
      <div :class="{ menuOpen: menuIsOpen }" class="hamburger-lines">
        <span class="line line1"></span>
        <span class="line line2"></span>
        <span class="line line3"></span>
      </div>
      <div :class="{ menuOpen: menuIsOpen }" class="menu-items">
        <li><router-link @click="toggleMenu" to="/">Home</router-link></li>
        <li>
          <router-link @click="toggleMenu" to="/experience"
            >Experience</router-link
          >
        </li>
        <li>
          <router-link @click="toggleMenu" to="/projects">Projects</router-link>
        </li>
        <li>
          <router-link @click="toggleMenu" to="/contact">Contact</router-link>
        </li>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      menuIsOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.menuIsOpen = !this.menuIsOpen;
      console.log(this.menuIsOpen);
      //return this.author.books.length > 0 ? "Yes" : "No";
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
nav {
  position: sticky;
  top: 0;
  text-transform: uppercase;
  z-index: 1;
  width: 100%;

  a {
    color: #000000;
    padding: 1rem;

    &:hover {
      font-weight: bolder;
    }
  }

  .nav-container {
    width: 100%;
    padding: 2rem;
    display: flex;
    justify-content: center;

    @media only screen and (max-width: 450px) {
      display: none;
    }
  }

  .mobile-nav-container {
    display: block;
    position: relative;
    height: 60px;

    @media only screen and (min-width: 450px) {
      display: none;
    }

    .checkbox {
      position: absolute;
      display: block;
      height: 2rem;
      width: 2rem;
      top: 2rem;
      right: 2rem;
      z-index: 5;
      opacity: 0;
      cursor: pointer;
    }

    .mobile-button {
      position: absolute;
      display: block;
      height: 2rem;
      width: 2rem;
      top: 2rem;
      right: 2rem;
      z-index: 5;
      opacity: 0;
      cursor: pointer;
    }

    .hamburger-lines {
      display: block;
      height: 25px;
      width: 32px;
      position: absolute;
      top: 2rem;
      right: 2rem;
      z-index: 2;
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      .line {
        display: block;
        height: 2px;
        width: 100%;
        border-radius: 10px;
        background: #0e2431;
      }

      .line1 {
        transform-origin: 0% 0%;
        transition: transform 0.4s ease-in-out;
      }

      .line2 {
        transition: transform 0.2s ease-in-out;
      }

      .line3 {
        transform-origin: 0% 100%;
        transition: transform 0.4s ease-in-out;
      }
    }

    .menu-items {
      background-color: blanchedalmond;
      box-shadow: inset 0 0 2000px rgba(255, 255, 255, 0.5);
      height: 100vh;
      width: 100%;
      transform: translate(-150%);
      display: flex;
      justify-content: center;
      flex-direction: column;
      transition: transform 0.5s ease-in-out;
      text-align: center;

      li {
        margin-bottom: 3rem;
        font-size: 1.5rem;
        font-weight: 500;
      }
    }
    .menuOpen {
      &.menu-items {
        transform: translateX(0);
      }

      .line1 {
        transform: rotate(45deg);
      }

      .line2 {
        transform: scaleY(0);
      }

      .line3 {
        transform: rotate(-45deg);
      }
    }
  }
}
</style>
