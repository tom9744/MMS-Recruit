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
  padding: 8px;

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

  &--video {
    height: 50vw;
    max-height: 720px;
    width: 100%;
  }

  &--list {
    list-style: none;

    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;

    padding: 0;
  }

  &--list-item {
  }
}

@media screen and (min-width: 400px) {
  .content {
    &--video {
      height: 40vw;
    }
  }
}

@media screen and (min-width: 780px) {
  .content {
    &--video {
      height: 35vw;
    }
  }
}

@media screen and (min-width: 1080px) {
  .content {
    &--video {
      height: 30vw;
    }
  }
}
</style>
