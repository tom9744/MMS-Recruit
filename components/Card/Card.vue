<template>
  <div class="card">
    <div class="card--header">
      <slot name="header" />
    </div>

    <div class="card--main">
      <slot name="main" />
    </div>

    <div class="card--footer">
      <slot name="footer" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.card {
  padding: 1rem;

  border: 1px solid gray;
  border-radius: 16px;

  &--header {
    margin-bottom: 1rem;
  }
}
</style>
