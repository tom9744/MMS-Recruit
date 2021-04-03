<template>
  <article class="content">
    <h2 class="content--title">
      <slot name="title" />
    </h2>

    <article class="content--body">
      <h3 class="content--subtitle">
        <slot name="subtitle" />
      </h3>

      <p class="content--paragraph">
        <slot name="paragraph" />
      </p>

      <slot />
    </article>
    <!-- Content Body -->
  </article>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.content {
  &--title {
    margin-bottom: 2rem;

    text-shadow: 2px 2px lightgray;
  }

  &--body {
    padding: 8px;
  }

  &--subtitle {
    margin-bottom: 1rem;
  }

  &--paragraph {
    margin-bottom: 1rem;
  }
}
</style>
