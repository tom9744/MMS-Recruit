<template>
  <li
    class="instrument"
    :class="isPlaying ? 'instrument__playing' : ''"
    @click="playSound"
  >
    <img
      class="instrument--icon"
      :src="require(`@/assets/imgs/instruments/${fileName}`)"
      :alt="instrumentType"
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
    fileName: {
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

  computed: {
    audioFilePath() {
      return `${this.fileName.split('.')[0]}.wav`
    },
  },

  mounted() {
    const soundFile = require(`@/assets/sounds/${this.audioFilePath}`)
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
  height: 100px;
  width: 100px;

  margin: 1rem;

  background-color: white;
  border-radius: 50%;

  transition: all 0.25s ease;

  cursor: pointer;

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
