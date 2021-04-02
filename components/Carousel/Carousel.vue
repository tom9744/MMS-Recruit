<template>
  <section class="carousel">
    <Slider :image-file-names="imageFileNames" :interval="3.5" />

    <h1 class="carousel--slogan">
      신새벽의 벅찬 가슴으로 민중의 새날을 노래하는 공과대 노래패, 목멱성
    </h1>
  </section>
</template>

<script>
import Slider from '@/components/Carousel/Slider'

export default {
  components: {
    Slider,
  },

  data() {
    return {
      imageFileNames: [
        'carousel_1.jpeg',
        'carousel_2.jpeg',
        'carousel_3.jpeg',
        'carousel_4.jpeg',
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.carousel {
  height: 100vh;
  width: 100vw;

  position: relative;

  &--slogan {
    position: absolute;
    top: 50%;
    left: 50%;

    width: 80%;

    color: white;

    text-align: center;

    transform: translate(-50%, -50%);
  }
}

@media screen and (min-width: 400px) {
  .carousel {
    height: 95vh;
  }
}

@media screen and (min-width: 780px) {
  .carousel {
    height: 90vh;
  }
}

@media screen and (min-width: 1080px) {
  .carousel {
    height: 85vh;
  }
}
</style>
