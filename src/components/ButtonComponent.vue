<template>
    <button :class="buttonClass" @click="handleClick">
      <slot></slot> 
    </button>
  </template>
  
  <script>
  export default {
    name: 'ButtonComponent',
    props: {
      type: {
        type: String,
        default: 'primary' // makes the default type 'primary'
      },
      onClick: {
        type: Function,
        default: () => {}
      }
    },
    computed: {
      buttonClass() {
        return {
          'btn': true,
          'btn-primary': this.type === 'primary',
          'btn-secondary': this.type === 'secondary',
          'btn-danger': this.type === 'danger'
        };
      }
    },
    methods: {
      handleClick() {
        this.onClick();
      }
    }
  }
  </script>
  
  <style scoped>
  .btn {
    display: inline-block;
    border: none;
    padding: 5px 25px;
    margin: 0;
    text-decoration: none;
    color: #ffffff;
    border-radius: 25px;
    font-size: 1rem;
    cursor: pointer;
    text-align: center;
    transition: background 250ms ease-in-out, transform 150ms ease;
    -webkit-appearance: none;
    -moz-appearance: none;
  }
  
  .btn-primary {
    background: #351C0C;
  }
  
  .btn-secondary {
    background: #6AA84F;
    color: #351C0C;
  }
  
  .btn-danger {
    background: #cc0000;
    color: #351C0C;
  }
  
  .btn:hover, .btn:focus {
    background: #ffffff;
    color: #351C0C;
    border: 1px solid #351C0C;
  }
  
  .btn:focus {
    outline: 1px solid #fff;
    outline-offset: -4px;
  }
  
  .btn:active {
    transform: scale(0.99);
  }
  </style>
  