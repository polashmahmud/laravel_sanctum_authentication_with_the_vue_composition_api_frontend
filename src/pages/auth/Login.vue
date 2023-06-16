<template>
  <h1 class="text-xl font-medium text-center">Login</h1>
  {{ user }}
  {{ authenticated }}
  <form v-on:submit.prevent="login(form)">
    <div class="mb-3">
      <label for="email" class="leading-7 text-sm text-gray-600">Email</label>
      <input v-model="form.email" type="email" name="email" id="email"
             class="w-full bg-white rounded border border-gray-300 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-200 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
    </div>
    <div class="mb-3">
      <label for="password" class="leading-7 text-sm text-gray-600">Password</label>
      <input v-model="form.password" type="password" name="password" id="password"
             class="w-full bg-white rounded border border-gray-300 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-200 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
    </div>
    <div class="mb-3">
      <button
          class="text-white w-full bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">
        Login
      </button>
    </div>
  </form>
</template>

<script setup>
import {reactive} from "vue";
import useAuth from "../../auth/useAuth.js";

const { login, getUser: user, getAuthenticated: authenticated } = useAuth()

const form = reactive({
  email: 'polashmahmud@gmail.com',
  password: 'password'
})


</script>