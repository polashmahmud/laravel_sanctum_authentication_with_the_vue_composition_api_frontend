<template>
  <nav>
    <router-link to="/">Home</router-link>
    <router-link to="/dashboard">Dashboard</router-link>
  </nav>
  <router-view></router-view>
</template>

<script setup>
import { RouterView, RouterLink} from "vue-router";
</script>
