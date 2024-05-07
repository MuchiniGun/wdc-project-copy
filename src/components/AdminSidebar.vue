<template>
 <nav class="admin-sidebar">
    <div class="admin-sidebar-wrapper">

<div class="dashboard-bubble-wrapper">
    <h1 class="dashboard-title">Admin Dashboard</h1>
</div>


    <button class='admin-btn'>
      <img src="@/components/icons/home.svg" alt="Home Icon">
      My Details
    </button>
    <button class='admin-btn'>
      <img src="@/components/icons/group.svg" alt="Group Icon">
      Organisations
    </button>
    <button class='admin-btn'>
      <img src="@/components/icons/user.svg" alt="User Icon">
      Users
    </button>
    <button class='admin-btn'>
      <img src="@/components/icons/games.svg" alt="Admin Icon">
      View Admins
    </button>
    <button class='admin-btn'>
      <img src="@/components/icons/add.svg" alt="Add Icon">
      Create Admins
    </button>
    </div>
</nav>
  </template>
  
  <script>
  import ButtonComponent from './ButtonComponent.vue'
  
  export default {
    name: 'AdminSidebar',
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

.dashboard-bubble-wrapper {
    align-items: center;
    background-color: red;
    border-radius: 10px;
    height: 45px;
    width: 250px;
    margin-bottom: 25px;
}

.dashboard-title {
    font-size: 32px;
    color: white;
    text-align: center;
}

.admin-sidebar-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: white;
    height: 32rem;
    width: 17rem;
    border-radius: 10px;
    padding: 1rem;
}

  .admin-sidebar {
      height: auto;
      width: 60vw;
      display: flex;
      flex-direction: column;
      align-items: left;
      justify-content: space-around;
      padding: 20px; 
      border-radius: var(--border-radius);
  }
  
  .admin-btn {
      color: var(--color-brown);
      background-color: white;
      border-radius: 10px;
      border: none;  
      padding: 10px 20px; 
      margin-top: 10px;
      margin-bottom: 10px;
      width: 230px; 
      display: flex;  
      align-items: center;  
      justify-content: start;  
      font-size: 20px;
      cursor: pointer;  
      transition: background-color 0.3s;  
  }
  
  .admin-btn:hover {
      background-color: #e6e6e6;  
  }
  
  .admin-btn img {
      margin-right: 12px;  
      height: 24px; 
      width: 24px; 
  }

  .admin-btn img {
    margin-right: 12px;  
    height: 45px; 
    width: 45px;  
}

  </style>
  