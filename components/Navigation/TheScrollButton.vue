<template>
  <button class="scroll-btn" @click="scrollToTop">
    <fa class="scroll-btn--icon" :icon="fas.faAngleDoubleUp" />
  </button>
</template>

<script>
import { fas } from '@fortawesome/free-solid-svg-icons'

export default {
  computed: {
    fas() {
      return fas
    },
  },
  methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' })
    },
  },
}
</script>

<style lang="scss" scoped>
.scroll-btn {
  position: fixed;
  bottom: 16px;
  right: 16px;

  height: 48px;
  width: 48px;

  border: none;
  border-radius: 50%;

  background-color: rgba(0, 0, 0, 0.25);

  &--icon {
    font-size: 1.5rem;
    font-weight: bold;
    color: white;
  }
}
</style>
