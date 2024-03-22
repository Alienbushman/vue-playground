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
  border: 1px solid #fff

.front
  transform: translateZ(50px)
  background-color: #3498db

.back
  transform: rotateY(180deg) translateZ(50px)
  background-color: #3498db

.left
  transform: rotateY(-90deg) translateZ(50px)
  background-color: #3498db

.right
  transform: rotateY(90deg) translateZ(50px)
  background-color: #3498db

.top
  transform: rotateX(90deg) translateZ(50px)
  background-color: #3498db

.bottom
  transform: rotateX(-90deg) translateZ(50px)
  background-color: #3498db

@keyframes spin
  from
    transform: rotateX(0) rotateY(0) rotateZ(0)
  to
    transform: rotateX(360deg) rotateY(360deg) rotateZ(360deg)
</style>
