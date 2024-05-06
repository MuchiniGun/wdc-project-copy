<template>
    <div class="post-card-wrapper">
        <h3 id="is-new">NEW</h3>
        <div class="post-title">
            <h1>{{ title }}</h1> 
        </div>
        <div class="post-content">
            {{ content }} 
        </div>
    </div>
</template>

<script>
export default {
  name: 'PostComponent',
  props: {
    title: {
      type: String,
      required: true,
      default: 'random title'
    },
    content: {
      type: String,
      required: true,
      default: 'random content'
    }
  }
}
</script>
  
<style scoped>
.post-card-wrapper {
    background-color: #fff;
    height: fit-content;
    width: 60vw;
    padding: 10px;
    display: flex;
    flex-direction: column;
    border-radius: var(--border-radius);
}

#is-new {
    color: var(--color-green);
}

.post-title {
    border-bottom: 1px solid grey;
    margin-bottom: 0.8rem;
}
</style>
