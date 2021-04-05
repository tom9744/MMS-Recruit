<template>
  <ul class="info-list">
    <li
      v-for="(info, idx) of informations"
      :key="idx"
      class="info-list--listitem"
    >
      <InfoListItem :information="info" />
    </li>
  </ul>
</template>

<script>
import InfoListItem from '@/components/Recruit/InfoListItem'

export default {
  components: {
    InfoListItem,
  },

  props: {
    informations: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.info-list {
  list-style: none;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  padding: 0;

  &--listitem {
    width: 100%;

    margin: 0.5rem 0;
  }
}

@media screen and (min-width: 780px) {
  .info-list {
    flex-direction: row;

    &--listitem {
      flex: 1;

      height: 260px;

      margin: 0 0.5rem;
    }
  }
}
</style>
