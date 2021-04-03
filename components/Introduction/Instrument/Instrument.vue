<template>
  <li class="instrument">
    <div class="instrument--overlay"></div>
    <div class="instrument--icon">
      <slot />
    </div>
  </li>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.instrument {
  position: relative;

  height: 100px;
  width: 100px;

  margin: 16px;

  background-color: white;
  border-radius: 50%;

  box-shadow: 0px 0px 10px -2px black;

  &--icon {
    height: 100%;
    width: 100%;

    display: flex;
    align-items: center;
    justify-content: center;
  }

  &--overlay {
    position: absolute;

    height: 100%;
    width: 100%;

    background-color: black;
    opacity: 0.25;

    border-radius: 50%;
  }
}
</style>
