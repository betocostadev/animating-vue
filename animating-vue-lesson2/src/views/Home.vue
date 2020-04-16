<template>
  <div class="home">
    <button @click="toggleModal">Open</button>
    <transition name="fade">
      <div v-if="isOpen" class="modal">
        <button @click="toggleModal">Close</button>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    }
  },
  methods: {
    toggleModal() {
      this.isOpen = !this.isOpen
    }
  }
}
</script>

<style>
/* How to start */
.fade-enter {
  opacity: 0;
}
/* How the transition should happen */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.75s ease-out;
}

.fade-leave-to {
  opacity: 0;
}
</style>
