<template>
  <li
    class="activity"
    :class="isIntersecting ? 'activity__visible' : ''"
    :style="imageStyle"
    @mouseover="onEnter"
    @mouseleave="onLeave"
  >
    <h4 class="activity--name">{{ isHover ? name : month }}</h4>
  </li>
</template>

<script>
export default {
  props: {
    month: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    fileName: {
      type: String,
      required: true,
    },
  },

  data() {
    return {
      isHover: false,
      isIntersecting: null,

      observer: null,
      observerOption: {
        threshold: 0,
      },
    }
  },

  computed: {
    // Vue Loader로 이미지를 불러오기 위해서 require() 메서드로 이미지를 모듈 형태로 불러온다.
    imageStyle() {
      return {
        background:
          'linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url(' +
          require(`@/assets/imgs/activities/${this.fileName}`) +
          ')',
        backgroundSize: 'cover',
        backgroundPosition: 'center center',
      }
    },
  },

  mounted() {
    this.observer = new IntersectionObserver(([entry]) => {
      this.isIntersecting = entry.isIntersecting
    }, this.observerOption)

    this.observer.observe(this.$el)
  },

  destroyed() {
    this.observer.disconnect()
  },

  methods: {
    onEnter() {
      this.isHover = true
    },
    onLeave() {
      this.isHover = false
    },
  },
}
</script>

<style lang="scss" scoped>
.activity {
  display: flex;
  align-items: center;
  justify-content: center;

  height: 150px;
  width: 100%;

  margin: 6px 0px;

  color: white;

  opacity: 0;

  transition: opacity 0.75s ease-in;

  &__visible {
    opacity: 1;

    background: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0));
  }
}

@media screen and (min-width: 1080px) {
  .activity {
    height: 300px;
    width: auto;

    margin: 0px 6px;

    flex: 1;
  }
}
</style>
