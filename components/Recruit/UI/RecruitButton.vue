<template>
  <button class="recruit-button" @click="openGoogleForm">
    <slot>지원하기</slot>
  </button>
</template>

<script>
export default {
  methods: {
    openGoogleForm() {
      window.open('https://forms.gle/14UzTR1D8xpXUi5p8', '_blank')
    },
  },
}
</script>

<style lang="scss" scoped>
.recruit-button {
  text-decoration: none;
  border: none;
  outline: none;

  cursor: pointer;

  height: 32px;
  width: 100%;

  font-weight: bold;
  color: white;
  background-color: rgb(65, 65, 190);
  border-radius: 16px;
}
</style>
