<template>
    <footer>
      <a href="https://github.com/Estridha"><img src="@/assets/icons/github.svg" alt="GitHub logo"/></a>
      <a href="https://www.linkedin.com/in/estridhassbring/"><img src="@/assets/icons/linkedin.svg" alt="LinkedIn logo"/></a>
    </footer>
  </template>
  
  <script>
  export default {
    name: "AppFooter",

  };
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  footer {
    display: flex;
    justify-content: center;
    width: 100%;
    padding-bottom: 5px;
  
    img {
      margin: 0 1rem;
      font-weight: bold;
      color: #000000;
      text-decoration: none;
  
      &.router-link-exact-active {
        color: #ffa321;
      }
    }
  }
  </style>
  