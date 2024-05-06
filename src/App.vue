<template>
  <div id="app">
    <div>
      <Navbar />
      <div>
        <GeneralBranchCard
          profile-picture="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTLX8mDWYtskMihbIjr7g7DrDvZXdfC5BfAlSLwMOVJzw&s"
          branch-name="Green'Fingers"
          branch-address="37 Plantation Road, Sefton Park, Adelaide, SA 5083, Australia"
          about-text="A local group dedicated to beautifying urban 
          areas through community-led gardening projects."
          :is-private="true"
          number-of-members="16000"
        />
        <GeneralBranchCard
          profile-picture="https://images.ctfassets.net/hrltx12pl8hq/28ECAQiPJZ78hxatLTa7Ts/2f695d869736ae3b0de3e56ceaca3958/free-nature-images.jpg?fit=fill&w=1200&h=630"
          branch-name="Arry"
          branch-address="runs"
          about-text="lol"
          :is-private="true"
          number-of-members="1"
        />
        <div>
          <ButtonComponent
            type="primary"
            :onClick="joinBranch"
          >
            Join
          </ButtonComponent>
          <ButtonComponent
            type="secondary"
            :onClick="createAdmin"
          >
            Create Admin
          </ButtonComponent>
          <ButtonComponent
            type="danger"
            :onClick="discard"
          >
            Discard
        </ButtonComponent>
        </div>
        <PostComponent 
          title="Furry Friends Await: Join Paws and Plays Today!"
          content="Looking for a way to lend a helping hand? At 
          Paws and Plays, we're on a mission to connect passionate 
          animal lovers with volunteer opportunities that make a 
          real difference. Whether it's walking shelter dogs, 
          socializing with cats, or assisting with adoption events, 
          your time and love can transform the lives of our furry 
          friends in need. Join us today and let's make every paw 
          count!"
        />
      </div>

    </div>
    
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import GeneralBranchCard from "./components/GeneralBranchCard.vue"
import ButtonComponent from './components/ButtonComponent.vue'
import PostComponent from './components/PostComponent.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    GeneralBranchCard,
    ButtonComponent,
    PostComponent
  },
  methods: {
    joinBranch() {
      alert('Joining Branch...');
    },
    createAdmin() {
      alert('Creating an admin...');
    },
    discard() {
      alert('Discarding...');
    }
  }
}
</script>

<style>
#app {
  font-family: 'lilita one', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 50px;
  background-color: rgb(95, 95, 95);
  height: 100vh;
  width: 100vw;
}
</style>
