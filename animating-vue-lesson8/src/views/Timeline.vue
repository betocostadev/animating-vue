<template>
  <div>
    <img class="runner first" src="../assets/runner.png" alt="runner" />
    <img class="runner second" src="../assets/runner.png" alt="runner" />
    <img class="runner third" src="../assets/runner.png" alt="runner" />
  </div>
</template>

<script>
import gsap from 'gsap'

export default {
  mounted() {
    // timeline will go here
    let tl = gsap.timeline({ repeat: -1, repeatDelay: 1 })
    tl.to('.first', { x: 800, duration: 4, ease: 'expo.out' })
    tl.to('.second', { x: 800, duration: 5, ease: 'expo.out' }, '<')
    tl.to('.third', { x: 800, duration: 3, ease: 'expo.out' }, '-=4.6')
  }
}
</script>

<style scoped>
.runner {
  display: block;
  height: 5em;
  width: 5em;
  margin-top: 1.5em;
}
</style>
