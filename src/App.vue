<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <h1>My fitness app</h1>
  <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
  </nav>
  <RouterView></RouterView>
 </template>
 <style scoped>
nav{
  display: flex;

}
nav >*{
  display: flex;
  margin: 5px;
}
</style>
