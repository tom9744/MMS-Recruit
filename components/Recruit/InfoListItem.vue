<template>
  <Card class="detail">
    <template #header>
      <h3 class="detail--title">{{ information.title }}</h3>
    </template>

    <template #main>
      <p v-if="information.para" class="detail--paragraph">
        {{ information.para }}
      </p>

      <ul v-if="information.list" class="detail--list">
        <li v-for="(talent, idx) of information.list" :key="idx" class="talent">
          {{ talent }}
        </li>
      </ul>

      <em v-if="information.emphasize" class="detail--emphasize">
        {{ information.emphasize }}
      </em>
    </template>
  </Card>
</template>

<script>
import Card from '~/components/Card/Card'

export default {
  components: {
    Card,
  },

  props: {
    information: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.detail {
  &--title {
    margin-bottom: 1rem;
  }

  &--list {
    list-style: none;

    padding: 0;
  }

  &--emphasize {
    font-size: 0.8rem;
  }
}
</style>
