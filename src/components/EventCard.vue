<template>
    <div class="event-card-wrapper">
        <div class="event-card-info">
            <div class="event-card-photo-wrapper">
                <img
                    :src="eventPhoto"
                    height="50"
                    width="50"
                    class="event-card-photo"
                    alt="Event Photo"
                />
            </div>
            <div class="event-details">
                <span>
                    <img 
                        src="@/components/icons/location-icon.svg" 
                        height="15" 
                        width="15" 
                        title="Location icon'"
                        alt="location icon"
                    />
                    {{ location }}
                </span>
                <span>
                    <img 
                        src="@/components/icons/clock-icon.svg" 
                        height="15" 
                        width="15" 
                        title="Location icon'"
                        alt="location icon"
                    />
                    {{ time }}
                </span>
            </div>
        </div>
        <div class="event-card-title">
            <h1> {{ title }}</h1>
        </div>
        <div class="event-card-opt">
            <ButtonComponent
              type="primary"
              @onClick="RSVP"
            >
              RSVP
            </ButtonComponent>
            <span>{{ numRSVPS }} RSVPs!</span>
        </div>
    </div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue';

export default {
  name: 'EventCard',
  components: {
    ButtonComponent
  },
  props: {
    eventPhoto: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    location: {
      type: String,
      required: true
    },
    time: {
      type: String,
      required: true
    },
    numRSVPS: {
        type: String,
        required: true
    }
    
  },
    methods: {
      RSVP() {
        alert('you have RSVPd');
      }
    }
}
</script>
  
<style scoped>

.event-card-wrapper {
    display: flex;
    flex-direction: column;
      background-color: #fff;
      align-items: center;
      height: 14rem;
      width: 20rem;
      border-radius: 25px;
      padding: 12px;
      gap: 10px;
  }

.event-card-info {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 50%;
    width: 100%;
    gap: 2px;
}

.event-card-photo-wrapper {
    position: relative;
    height: 75%;
    width: 100%;
    overflow: hidden;
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.event-card-photo {
    width: 100%;
    height: auto;
    object-fit: center;
}

.event-details {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
}

.event-card-title h1 {
  text-align: center;
}

.event-card-opt {
  display: flex;
  flex-direction: column;
  gap: 2px;
  width: 100%;
}

.event-card-opt span {
  color: var(--color-green);
  text-align: center;
}


</style>
  
  