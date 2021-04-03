<template>
  <ul class="advantage-list">
    <li
      v-for="(advantage, idx) of advantages"
      :key="idx"
      class="advantage-list--item"
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
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;

  gap: 16px;
}

@media screen and (min-width: 1080px) {
  .advantage-list {
    align-items: baseline;
    flex-wrap: nowrap;

    &--item {
      flex: 1;

      height: 350px;
    }
  }
}
</style>
