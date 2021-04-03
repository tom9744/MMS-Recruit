<template>
  <iframe
    class="app-iframe"
    :src="source"
    :title="title"
    width="560"
    height="315"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</template>

<script>
export default {
  props: {
    source: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      default: 'YouTube Video Player',
    },
  },
}
</script>

<style lang="scss" scoped>
.app-iframe {
  height: 50vw;
  max-height: 720px;
  width: 100%;
}

@media screen and (min-width: 400px) {
  .app-iframe {
    height: 40vw;
  }
}

@media screen and (min-width: 780px) {
  .app-iframe {
    height: 35vw;
  }
}

@media screen and (min-width: 1080px) {
  .app-iframe {
    height: 30vw;
  }
}
</style>
