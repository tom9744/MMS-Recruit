<template>
  <img
    :src="require(`@/assets/icons/${source}`)"
    alt=""
    height="32"
    width="32"
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
