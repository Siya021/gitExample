<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/products">Soccer Stars</router-link>
  </nav>
  <footer></footer>
  <router-view/>
</template>

<script>

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
  background-color: navy ;
  color: white;
}

nav a {
  font-weight: bold;
  color: #ffffff;
}

nav a.router-link-exact-active {
  color: #2cb9d9;
}
</style>
