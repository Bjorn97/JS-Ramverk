<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: 'Montserrat', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
#nav {
    width: 70%;
    display: flex;
    justify-content: center;
    font-family: 'Montserrat', Helvetica, Arial, sans-serif;
}
#nav a {
    text-decoration: none;
    color: #000;
    padding: 10px;
}
</style>
