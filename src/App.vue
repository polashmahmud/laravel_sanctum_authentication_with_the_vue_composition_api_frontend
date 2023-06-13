<template>
  <form v-on:submit.prevent="login">
    <button type="submit">Login</button>
  </form>
</template>

<script setup>
import axios from "axios";

const login = async () => {
  await axios.get('/sanctum/csrf-cookie');
  await axios.post('/login', {
    email: 'polashmahmud@gmail.com',
    password: 'password'
  });
}
</script>
