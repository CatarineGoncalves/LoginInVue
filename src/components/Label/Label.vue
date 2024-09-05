<template>
    <label :for="id" class="label">
      {{ text }}
    </label>
  </template>
  
  <script>
  export default {
    name: 'Label',
    props: {
      id: {
        type: String,
        required: true
      },
      text: {
        type: String,
        required: true
      }
    }
  }
  </script>