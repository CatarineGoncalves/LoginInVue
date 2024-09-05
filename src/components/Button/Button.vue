<template>
  <button 
    class="loginButton" 
    :class="{ 'clicked': isClicked }"
    @click="handleClick"
  >
    <img src="./../../assets/entrar.png" alt="Login" />
    Login
  </button>
</template>

<script>
export default {
  name: 'Button',
  data() {
    return {
      isClicked: false
    };
  },
  methods: {
    handleClick() {
      this.isClicked = true;
      setTimeout(() => {
        this.isClicked = false;
      }, 300);
      this.$emit('click'); 
    }
  }
}
</script>

<style scoped>
  @import './Button.css';
</style>
