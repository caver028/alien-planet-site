<script setup>
import aliens from '../MOCK_DATA.js'
import Card from "./Card.vue";
import PrimaryTemplate from "../templates/PrimaryTemplate.vue";
</script>

<template>
  <primary-template header-img="alien-title.jpg">
    <h1>Welcome to Alien Planet, Select an Alien to Begin a Virtual Voyage</h1>

    <p v-for="(aliens, index) in aliens.aliens" :key="index">
      <card :environment="aliens.environment" :first-name="aliens.alien_name" />
    </p>
  </primary-template>
</template>

<style scoped>

</style>