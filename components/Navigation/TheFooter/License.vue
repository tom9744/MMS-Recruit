<template>
  <div class="license">
    <p>
      <strong><slot name="category" /></strong>

      <slot />
    </p>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.license {
  text-align: left;
}

@media screen and (min-width: 780px) {
  .license {
    text-align: center;
  }
}
</style>
