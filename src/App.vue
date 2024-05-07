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
        <PollCard 
          title="Should Event #1 Be Re-Scheduled?"
          content="Due to heavy rains predicted on the day of event 
          1, we are considering rescheduling this event to a later 
          date. However, if the community believes that it is important 
          to pursue this event, we can vote upon it.
          Due to heavy rains predicted on the day of event 
          1, we are considering rescheduling this event to a later 
          date. However, if the community believes that it is important 
          to pursue this event, we can vote upon it.
          Due to heavy rains predicted on the day of event 
          1, we are considering rescheduling this event to a later 
          date. However, if the community believes that it is important 
          to pursue this event, we can vote upon it."
        />
        <EventCard 
          eventPhoto="https://lh4.googleusercontent.com/Jko2qY8vT5da2GjL601whdRxiBXgJ5vhG7BTbYWCIUgDfzA65MyJMFBOd3XVl2Wdh4gQ4jGFC6zIPRHnPsCIbmj8nXaP0qve7_8LGzvM7oCJ62BnQLG1ryUowOF7P7E4qSmhT_UrrePtmE7V4tTZsn2Idc63H8J03eWhCzPfSMg5RkcVmeSEvGFOFKNHpg"
          title="Puppy Washing"
          location="Adelaide oval"
          time="10AM"
          numRSVPS="125"
        />
        <AdminSidebar />
      </div>

    </div>
    
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import GeneralBranchCard from "./components/GeneralBranchCard.vue"
import ButtonComponent from './components/ButtonComponent.vue'
import PostComponent from './components/PostComponent.vue'
import PollCard from './components/PollCard.vue';
import EventCard from './components/EventCard.vue';
import AdminSidebar from './components/AdminSidebar.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    GeneralBranchCard,
    ButtonComponent,
    PostComponent,
    PollCard,
    EventCard,
    AdminSidebar
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
  background-color: var(--color-pink);
  height: 100vh;
  width: 100vw;
}
</style>
