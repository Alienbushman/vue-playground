<script setup lang="ts">
</script>

<template>
  <div class="container">
    <div class="cube">
      <div class="side front"></div>
      <div class="side back"></div>
      <div class="side left"></div>
      <div class="side right"></div>
      <div class="side top"></div>
      <div class="side bottom"></div>
    </div>
  </div>
</template>

<style scoped lang="sass">
.container
  display: flex
  flex-direction: column
  justify-content: center
  align-items: center
  height: 100vh
  text-align: center

h1
  font-size: 2.5em
  margin-bottom: 20px

p
  font-size: 1.2em

.cube
  width: 100px
  height: 100px
  position: relative
  transform-style: preserve-3d
  animation: spin 5s infinite linear

.side
  position: absolute
  width: 100px
  height: 100px
  background-color: rgba(0, 0, 0, 0.2)

.front
  transform: translateZ(50px)
  background-color: #3498db

.back
  transform: rotateY(180deg) translateZ(50px)
  background-color: #e74c3c

.left
  transform: rotateY(-90deg) translateZ(50px)
  background-color: #2ecc71

.right
  transform: rotateY(90deg) translateZ(50px)
  background-color: #f1c40f

.top
  transform: rotateX(90deg) translateZ(50px)
  background-color: #9b59b6

.bottom
  transform: rotateX(-90deg) translateZ(50px)
  background-color: #34495e

@keyframes spin
  from
    transform: rotateY(0)
  to
    transform: rotateY(360deg)
</style>
