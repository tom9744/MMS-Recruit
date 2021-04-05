<template>
  <a
    class="app-anchor"
    :href="href"
    :title="title"
    :target="target"
    :rel="relation"
  >
    {{ title }}
  </a>
</template>

<script>
export default {
  props: {
    href: {
      type: String,
      required: true,
    },
    relation: {
      type: String,
      required: true,
    },
    isHttps: {
      type: Boolean,
      default: true,
    },
    title: {
      type: String,
      default: '',
    },
    target: {
      type: String,
      default: '_blank',
    },
  },
}
</script>

<style lang="scss" scoped>
.app-anchor {
  text-decoration: underline;
  cursor: pointer;

  color: rgb(0, 0, 0);

  transition: all 0.5s ease;

  &:hover {
    color: rgb(65, 65, 190);
  }
}
</style>
