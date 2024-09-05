<template>
  <div id="app">
    <main>
      <div class="loginContainer">
        <div class="inputBox">
          <Input id="email" v-model="email" inputType="email" label="E-mail" />
        </div>
        <div class="inputBox">
          <Input id="password" v-model="password" inputType="password" label="Senha" />
        </div>
        <div class="buttonBox">
          <Button @click="handleLogin" />
        </div>
      </div>
    </main>

    <Waves />
  </div>
</template>

<script>
import Input from './components/Input/Input.vue';
import Waves from './components/Waves/Waves.vue';
import Button from './components/Button/Button.vue';

export default {
  name: 'App',
  components: {
    Input,
    Waves,
    Button
  },
  data() {
    return {
      email: '',
      password: ''
    };
  },
  methods: {
    handleLogin() {
      if (this.email === '' || this.password === '') {
        alert('Não deve haver um campo nulo');
      } else {
        alert('Está Logado');
      }
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  background-color: #8EC5FC;
  background-image: linear-gradient(62deg, #8EC5FC 0%, #E0C3FC 100%);
  width: 100%;
  height: 100vh;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

main {
  width: 300px;
  height: 29vh;
  display: flex;
  flex-direction: column;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
}

.loginContainer div:nth-child(1) {
  margin-top: 10px;
}


.loginContainer {
  width: 90%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  place-self: center;
}

.inputBox {
  margin-bottom: 10px;
}


@media only screen and (max-width: 445px) {
  main {
    width: 90vw;
  }
}
</style>
