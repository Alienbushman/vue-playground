<template>
  <div class="container">
    <div class="sun">
      <div class="earth-orbit">
        <div class="earth">
          <div class="moon"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="sass">
.container
  display: flex
  flex-direction: column
  justify-content: center
  align-items: center
  height: 20vh
  text-align: center


.sun
  width: 20px
  height: 20px
  border-radius: 50%
  background-color: #fdd835
  position: relative

.earth-orbit
  width: 100px
  height: 100px
  position: absolute
  top: 50%
  left: 50%
  transform-origin: 0 0
  animation: orbit 10s linear infinite

.earth
  width: 20px
  height: 20px
  border-radius: 50%
  background-color: #1565c0
  position: absolute
  top: -10px
  left: calc(50% - 10px)

.moon
  width: 8px
  height: 8px
  border-radius: 50%
  background-color: #b0bec5
  position: absolute
  top: 12px
  left: calc(50% + 12px)
  animation: moonOrbit 5s linear infinite

@keyframes orbit
  from
    transform: rotate(0deg)
  to
    transform: rotate(360deg)

@keyframes moonOrbit
  from
    transform: rotate(0deg)
  to
    transform: rotate(360deg)
</style>
