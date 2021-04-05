<template>
  <ul class="advantage-list">
    <li
      v-for="(advantage, idx) of advantages"
      :key="idx"
      class="advantage-list--listitem"
    >
      <Card>
        <template #header>
          <h3>{{ advantage.subject }}</h3>
        </template>

        <template #main>
          <p>{{ advantage.description }}</p>
        </template>
      </Card>
    </li>
  </ul>
</template>

<script>
import Card from '~/components/Card/Card'

export default {
  components: {
    Card,
  },

  props: {
    advantages: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.advantage-list {
  list-style: none;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  &--listitem {
    width: 100%;

    margin: 0.5rem 0;
  }
}

@media screen and (min-width: 1080px) {
  .advantage-list {
    flex-direction: row;

    &--listitem {
      flex: 1;

      height: 350px;

      margin: 0 0.5rem;
    }
  }
}
</style>
