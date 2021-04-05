<template>
  <ul class="instrument-list">
    <Instrument
      v-for="(inst, idx) of instruments"
      :key="idx"
      :instrument-type="inst.type"
      :image-file-name="inst.fileName"
      :sound-file-name="inst.soundFile"
    />
  </ul>
</template>

<script>
import Instrument from '~/components/Introduction/Instrument/Instrument'

export default {
  components: {
    Instrument,
  },

  props: {
    instruments: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.instrument-list {
  list-style: none;

  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;

  gap: 16px;
  padding: 16px 0px;
}
</style>
