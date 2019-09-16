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
    .wrapper {
        width: 100%;
    }
    .boop {
        margin-left: 5%;
    }
    .wrapper .header {
        width: 100%;
        display: flex;
        margin-top: 10px;
    }
    .wrapper .header .name {
        width: 30%;
        text-align: center;
    }
     .wrapper .header nav {
        width: 70%;
        display: flex;
        justify-content: center;
    }
    .wrapper .header nav .link {
        width: 20%;
        text-align: center;
        border-top: 2px solid #8CB5CA;
        border-bottom: 2px solid #8CB5CA;
    }
    .wrapper .header nav .link:hover {
        transition: background-color 0.8s ease;
        background-color: #8CB5CA;
    }
    .wrapper .header nav .link .b {
        margin-top: 15px;
        font-size: 2em;
    }
    .wrapper .header nav .link a {
        text-decoration: none;
        color: #000;
        padding: 20px 0 20px 0;
    }
    .wrapper .header nav .link a h2 {
        margin: 0;
    }
    .dropdown-toggle {
        background-color: white!important;
        color: #000!important;
        width: 100%!important;
        height: 75px!important;
        font-family: Montserrat!important;
        font-size: 2em!important;
        border: 0!important;
    }

    .dropdown-toggle:hover {
        transition: background-color 0.8s ease!important;
        background-color: #8CB5CA!important;
        border: 0!important;
    }

    .show > .dropdown-toggle {
        background-color: #8CB5CA!important;
    }
    .show > #dropdown-1__BV_toggle_ {
        background-color: #8CB5CA !important;
        border: 0!important;
    }
</style>
