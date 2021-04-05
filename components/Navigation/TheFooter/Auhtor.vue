<template>
  <ul class="author">
    <li v-for="(info, idx) of authorInfo" :key="idx" class="author--info">
      <strong>{{ info.category }}</strong>

      <span v-if="info.text"> {{ info.text }} </span>

      <AppAnchor
        v-if="info.link"
        :href="info.link.href"
        :title="info.link.title"
      >
      </AppAnchor>
    </li>
  </ul>
</template>

<script>
import AppAnchor from '~/components/UI/AppAnchor'
export default {
  components: {
    AppAnchor,
  },

  props: {
    authorInfo: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.author {
  list-style: none;
}
</style>
