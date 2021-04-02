<template>
  <div class="slider">
    <div
      v-for="(imageId, idx) in numberOfImages"
      :key="idx"
      class="slider--item"
      :class="activeImageId === imageId ? 'slider--item__active' : ''"
      :style="imageStyles[idx]"
    ></div>
  </div>
</template>

<script>
export default {
  props: {
    imageFileNames: {
      type: Array,
      required: true,
    },
    interval: {
      type: Number,
      default: 5,
    },
  },

  data() {
    return {
      activeImageId: 1,
    }
  },

  computed: {
    numberOfImages() {
      return this.imageFileNames.length
    },

    // Vue Loader로 이미지를 불러오기 위해서 require() 메서드로 이미지를 모듈 형태로 불러온다.
    imageStyles() {
      return this.imageFileNames.map((fileName) => {
        return {
          background:
            'linear-gradient(rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.25)), url(' +
            require(`@/assets/${fileName}`) +
            ')',
          backgroundSize: 'cover',
          backgroundPosition: 'center top',
        }
      })
    },

    millisecondInterval() {
      return this.interval * 1000
    },
  },

  mounted() {
    this.slide()
  },

  methods: {
    slide() {
      setInterval(() => {
        const nextId = this.activeImageId + 1
        this.activeImageId = nextId < 5 ? nextId : 1
      }, this.millisecondInterval)
    },
  },
}
</script>

<style lang="scss" scoped>
.slider {
  position: relative;

  height: 100%;
  width: 100%;

  &--item {
    position: absolute;

    height: 100%;
    width: 100%;

    background-size: cover;
    background-position: center top;

    opacity: 0;
    transition: opacity 1s ease-in-out;

    &__active {
      opacity: 1;
    }
  }
}
</style>
