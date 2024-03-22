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
  justify-content: center
  align-items: center
  height: 10vh


.cube
  width: 50px
  height: 50px
  position: relative
  transform-style: preserve-3d
  animation: spin 5s infinite linear

.side
  position: absolute
  width: 50px
  height: 50px
  background-color: rgba(0, 0, 0, 0.2)
  border: 1px solid #fff

.front
  transform: translateZ(25px)
  background-color: #3498db

.back
  transform: rotateY(180deg) translateZ(25px)
  background-color: #3498db

.left
  transform: rotateY(-90deg) translateZ(25px)
  background-color: #3498db

.right
  transform: rotateY(90deg) translateZ(25px)
  background-color: #3498db

.top
  transform: rotateX(90deg) translateZ(25px)
  background-color: #3498db

.bottom
  transform: rotateX(-90deg) translateZ(25px)
  background-color: #3498db

@keyframes spin
  from
    transform: rotateX(0) rotateY(0) rotateZ(0)
  to
    transform: rotateX(360deg) rotateY(360deg) rotateZ(360deg)
</style>
