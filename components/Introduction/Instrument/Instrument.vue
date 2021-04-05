<template>
  <li
    class="instrument"
    :class="isPlaying ? 'instrument__playing' : ''"
    @click="playSound"
  >
    <img
      class="instrument--icon"
      :src="require(`@/assets/imgs/instruments/${imageFileName}`)"
      :alt="instrumentType"
      loading="lazy"
    />
  </li>
</template>

<script>
export default {
  props: {
    instrumentType: {
      type: String,
      required: true,
    },
    imageFileName: {
      type: String,
      required: true,
    },
    soundFileName: {
      type: String,
      required: true,
    },
  },

  data() {
    return {
      audio: null,

      isPlaying: false,
    }
  },

  mounted() {
    const soundFile = require(`@/assets/sounds/${this.soundFileName}`)
    const audio = new Audio(soundFile.default)
    audio.onplaying = () => {
      this.isPlaying = true
    }
    audio.onpause = () => {
      this.isPlaying = false
    }
    this.audio = audio
  },

  methods: {
    playSound() {
      this.isPlaying ? this.audio.pause() : this.audio.play()
    },
  },
}
</script>

<style lang="scss" scoped>
.instrument {
  height: 85px;
  width: 85px;

  margin: 1rem;

  cursor: pointer;

  background-color: white;
  border-radius: 50%;

  transition: all 0.25s ease;

  &--icon {
    height: 100%;
    width: 100%;

    padding: 1rem;

    display: flex;
    align-items: center;
    justify-content: center;
  }

  &__playing {
    animation: playing 0.5s infinite ease-in alternate;
  }

  &:hover {
    transform: scale(1.1);
  }
}

@keyframes playing {
  0% {
    box-shadow: 0px 0px 10px -5px rgb(65, 65, 190);
  }
  100% {
    box-shadow: 0px 0px 50px -5px rgb(65, 65, 190);
  }
}
</style>
