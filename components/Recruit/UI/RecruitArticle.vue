<template>
  <article class="recruit-article">
    <h2 class="recruit-article--title"><slot name="title" /></h2>

    <div class="recruit-article--content">
      <slot name="content" />
    </div>
  </article>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.recruit-article {
  width: 100%;

  padding: 5% 0;

  &--title {
    margin-bottom: 2rem;
  }
}
</style>
