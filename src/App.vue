<template>
  <div>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/contact">Contact</router-link>
  </nav>
  <router-view/>
</div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
}

nav {
  margin-top: 20px;
  font-size: 20px;
  font-family: "Cinzel";
  padding: 30px;
}

@font-face {
    font-family: 'Cinzel';
    src: url('~@/assets/fonts/Cinzel-VariableFont_wght.ttf') format('truetype');
  }

nav a {
  font-weight: bold;
  color: white;
  text-decoration-line: none;
  margin: 10px;
}

nav a.router-link-exact-active {
  color: #ffe600;
}
</style>
