<template>
    <div id="page2">
      <div>
        <Navbar />
        s
      </div>
    </div>
  </template>
  
  <script>
  import Navbar from './components/Navbar.vue'
  
  export default {
    name: 'Page2',
    components: {
      Navbar
    }
  }
  </script>
  
  <style>
  #page2 {
    font-family: 'lilita one', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    margin-top: 50px;
    background-color: rgb(255, 255, 255);
    height: 100vh;
    width: 100vw;
  }
  </style>
  