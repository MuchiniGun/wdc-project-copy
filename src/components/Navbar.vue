<template>
    <nav class="navbar">
        <div class="logo-wrapper">
            <img src="@/components/icons/lock-icon.svg" alt="Together.org Logo" class="navbar-logo">
            <h1 class="navbar-title">Together.org</h1>
        </div>
      <div class="navbar-links">
        <ButtonComponent
          type="secondary"
          @onClick="findOpportunity"
        >
          Find an Opportunity
        </ButtonComponent>
        <ButtonComponent
          type="primary"
          @onClick="signUp"
        >
          Sign Up
        </ButtonComponent>
        <img src="@/components/icons/lock-icon.svg" alt="Profile" class="user-icon">
      </div>
    </nav>
  </template>
  
  <script>
  import ButtonComponent from './ButtonComponent.vue'
  
  export default {
    name: 'Navbar',
    components: {
      ButtonComponent
    },
    methods: {
      findOpportunity() {
        alert('Finding opportunities...');
      },
      signUp() {
        alert('Sign up process...');
      }
    }
  }
  </script>
  
  <style scoped>
  .navbar {
    height: 4rem;
    width: 60vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: var(--color-background); 
    padding: 10px 20px;
    border-radius: var(--border-radius);
    outline: 2px solid #000; 
  }

  .logo-wrapper {
    display: flex;
    align-items: center;
    gap: 10px;
  }
  
  .navbar-logo {
    height: 50px;
    width: auto;
  }
  
  .navbar-title {
    margin: 0;
    color: #532020; /* Dark green for contrast */
    font-size: 24px;
  }
  
  .navbar-links {
    display: flex;
    align-items: center;
    gap: 10px;
  }
  
  .user-icon {
    height: 40px;
    width: auto;
  }
  </style>
  