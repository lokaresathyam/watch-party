<template>
    <div>
      <input type="email" v-model="email" placeholder="Email">
      <input type="password" v-model="password" placeholder="Password">
      <button @click="login">Login</button>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const email = ref('');
      const password = ref('');
  
      const login = () => {
        // Authentication logic here
      };
  
      return {
        email,
        password,
        login
      };
    }
  };
  </script>
  