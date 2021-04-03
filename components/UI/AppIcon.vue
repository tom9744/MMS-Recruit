<template>
  <img
    :src="require(`@/assets/icons/${source}`)"
    :alt="alter"
    :height="size"
    :width="size"
  />
</template>

<script>
export default {
  props: {
    source: {
      type: String,
      required: true,
    },
    size: {
      type: Number,
      required: true,
    },
    alter: {
      type: String,
      default: 'Icon Image',
    },
  },
}
</script>

<style></style>
