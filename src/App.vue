<template>
  <div id="app" >
    <h1>Witaj w systemie zapisów na zajęcia</h1>
    <h3>Zaloguj się e-mailem</h3>
  
<div v-if="!isAuthenticated">
  <input type="email" v-model ="email">
  <button @click="logIn()">Wchodzę</button>
</div>

<div v-else>
  <h2>Zalogowany jako {{email}}</h2>
  <button @click="logOut()">Wyloguj</button>
</div>
    </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      email: "",
      isAuthenticated: false
    };
  },
  methods: {
    logIn() {
      this.isAuthenticated = true;
    },
    logOut() {
      this.isAuthenticated = false;
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: bold;
  font-size: 2000 px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
