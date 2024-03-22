<script setup lang="ts">
import EarthRotation from "../components/EarthRotation.vue";
</script>

<template>
  <div class="container">
    <h1>Very basic landing page</h1>
    <p>Welcome to our website!</p>
    <color-switching-cube></color-switching-cube>
    <rotating-cube></rotating-cube>
    <earth-rotation></earth-rotation>
  </div>

</template>

<style scoped lang="sass">
.container
  display: flex
  flex-direction: column
  justify-content: center
  align-items: center
  height: 50vh
  text-align: center

h1
  font-size: 2.5em
  margin-bottom: 20px

p
  font-size: 1.2em
</style>
