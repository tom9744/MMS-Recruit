<template>
  <div class="card" :class="isIntersecting ? 'card__visible' : ''">
    <div class="card--header">
      <slot name="header" />
    </div>

    <div class="card--main">
      <slot name="main" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      observer: null,
      observerOption: {
        threshold: 0,
      },
      isIntersecting: null,
    }
  },

  mounted() {
    this.observer = new IntersectionObserver(([entry]) => {
      this.isIntersecting = entry.isIntersecting
    }, this.observerOption)

    this.observer.observe(this.$el)
  },

  destroyed() {
    this.observer.disconnect()
  },
}
</script>

<style lang="scss" scoped>
.card {
  height: 100%;
  width: 100%;

  padding: 1rem;

  border: 1px solid gray;
  border-radius: 16px;
  box-shadow: 0px 2px 6px -2px gray;

  opacity: 0;

  &--header {
    margin-bottom: 1rem;
  }

  &__visible {
    opacity: 1;

    animation: popIn 0.5s ease forwards;
  }
}

@keyframes popIn {
  0% {
    transform: scale(0.5);
  }
  75% {
    transform: scale(1.05);
  }
  100% {
    transform: scale(1);
  }
}
</style>
