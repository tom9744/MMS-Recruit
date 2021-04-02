<template>
  <section class="main-section">
    <slot />
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.main-section {
  width: 100%;

  padding: 30% 5%;

  display: flex;
  align-items: center;
  justify-content: center;

  &:nth-child(odd) {
    background-color: #f3f3f3;
  }
}

@media screen and (min-width: 400px) {
  .main-section {
    padding: 25% 15%;
  }
}

@media screen and (min-width: 780px) {
  .main-section {
    padding: 20% 20%;
  }
}

@media screen and (min-width: 1080px) {
  .main-section {
    padding: 15% 20%;
  }
}
</style>
