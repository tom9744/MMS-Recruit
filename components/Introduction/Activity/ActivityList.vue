<template>
  <ul class="activity-list">
    <Activity
      v-for="(activity, idx) of activities"
      :key="idx"
      :month="activity.month"
      :name="activity.name"
      :description="activity.description"
      :file-name="activity.fileName"
    >
    </Activity>
  </ul>
</template>

<script>
import Activity from '~/components/Introduction/Activity/Activity'
export default {
  components: {
    Activity,
  },

  props: {
    activities: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.activity-list {
  list-style: none;

  display: flex;
  flex-direction: column;
}

@media screen and (min-width: 1080px) {
  .activity-list {
    flex-direction: row;
  }
}
</style>
