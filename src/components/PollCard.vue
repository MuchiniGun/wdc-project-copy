<template>
    <div class="poll-card-wrapper">
        <div class="poll-card-title">
            <h1> {{ title }}</h1>
        </div>
        <div class="poll-card-content">
            <p>{{ content }}</p>
        </div>
        <div class="poll-card-opts">
          <div class="poll-card-opt">
            <ButtonComponent
              type="primary"
              @onClick="voteYes"
            >
              Yes
            </ButtonComponent>
            <span>Yes Votes: {{ yesVotes }}</span>
          </div>
          <div class="poll-card-opt">
            <ButtonComponent
              type="primary"
              @onClick="voteNo"
            >
              No
            </ButtonComponent>
            <span>Yes Votes: {{ noVotes }}</span>
          </div>
        </div>
    </div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue';

export default {
  name: 'PollCard',
  components: {
    ButtonComponent
  },
  props: {
    title: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    }
  },
    methods: {
      voteYes() {
        alert('Yes!');
      },
      signUp() {
        alert('No!');
      }
    }
}
</script>
  
<style scoped>
.poll-card-wrapper {
  display: flex;
  flex-direction: column;
    background-color: #fff;
    align-items: center;
    height: 14rem;
    width: 20rem;
    border-radius: 25px;
    padding: 1rem;
    gap: 10px;
}

.poll-card-title {
  background-color: var(--color-brown);
  border-radius: 12px;
}

.poll-card-title h1 {
  text-align: center;
  color: #fff;
}

.poll-card-content p {
    color: var(--color-brown);
    overflow: hidden;
    display: -webkit-box;
    -webkit-line-clamp: 6;
    -webkit-box-orient: vertical;
    text-overflow: ellipsis;
    text-align: center;
}

.poll-card-opts {
  display: flex;
  flex-direction: row;
  justify-content: center;
  width: 100%;
  gap: 5px;
}

.poll-card-opt {
  display: flex;
  flex-direction: column;
  gap: 2px;
  width: 100%;
}

.poll-card-opt span {
  color: var(--color-green);
  text-align: center;
}


</style>
  
  