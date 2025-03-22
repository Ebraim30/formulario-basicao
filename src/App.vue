<script setup>
import Navbar from './components/Navbar.vue';
import Home from './components/Home.vue';
import Category from './components/Category.vue';
</script>

<template>
  <Navbar />
  <div class="container overflow-x-hidden">
    <Home />
  </div>
  <div class="overflow-x-hidden">
    <Category />
  </div>
</template>
