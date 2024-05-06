<template>
    <div class="branch-feed-card-wrapper">
        <div class="branch-feed-card-info">
            <img
                :src="profilePicture"
                height="50"
                width="50"
                class="branch-feed-card-profile-photo"
                alt="Profile Photo"
            />
            <span id="info-txt">
                <h1>{{ branchName }}</h1>
                <h4>{{ branchAddress }}</h4>
            </span>
        </div>
        <div class="branch-feed-card-about">
            <h4>About</h4>
            <p>{{ aboutText }}</p>
        </div>
        <div class="branch-feed-card-join-info">
            <button class="default-btn">
                Join
            </button>
            <img :src="isPrivate ? lockIcon : unlockIcon" 
                height="25" 
                width="25" 
                :title="isPrivate ? 'Private branch' : 'Public branch'"
                alt="Public or Private Branch" />
            <div class="number-of-members" title="number of branch members">
                <img src="@/components/icons/person-icon.svg" height="30" width="30" alt="Members Icon"/>
                <h5>{{ numberOfMembers }}</h5>
            </div>
        </div>
    </div>
</template>

<script>
  import lockIcon from '@/components/icons/lock-icon.svg';
  import unlockIcon from '@/components/icons/person-icon.svg';

export default {
  name: 'GeneralBranchCard',
  props: {
    profilePicture: {
      type: String,
      required: true
    },
    branchName: {
      type: String,
      required: true
    },
    branchAddress: {
      type: String,
      required: true
    },
    aboutText: {
      type: String,
      required: true
    },
    isPrivate: {
      type: Boolean,
      required: true
    },
    numberOfMembers: {
      type: [String, Number],
      required: true
    }
  }, 
  data() {
    return {
      lockIcon,
      unlockIcon
    };
  }
}
</script>
  
<style scoped>
.branch-feed-card-wrapper {
  display: flex;
  flex-direction: column;
    background-color: #D0DD9A;
    height: 15rem;
    width: 25rem;
    border-radius: 25px;
    padding: 1rem;
}

.branch-feed-card-info {
    display: flex;
    align-items: center;
    height: 35%;
    gap: 10px;
}

.branch-feed-card-info span {
    color: red;
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    text-align: start;
}

.branch-feed-card-profile-photo {
    border-radius: 50%; 
    width: 50px;       
    height: 50px;      
    object-fit: cover; 
}


.branch-feed-card-about {
    margin-top: 10px;
    margin-left: 20px;
    height: 40%;
}

.branch-feed-card-about p {
    color: #fff;
    overflow: hidden;
    display: -webkit-box;
    -webkit-line-clamp: 6;
    -webkit-box-orient: vertical;
    text-overflow: ellipsis;
}


.branch-feed-card-join-info {
    display: flex;
    flex-direction: row;
    align-items: center;
    height: 25%;
    gap: 10px;
}

.branch-feed-card-join-info .number-of-members {
    display: flex;
    flex-direction: row;
    align-items: center;
}
</style>
  
  