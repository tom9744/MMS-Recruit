<template>
  <header class="header">
    <div class="header--logo">
      <nuxt-link to="/">
        <img src="@/assets/logo.svg" alt="MMS Logo" height="40px" />
      </nuxt-link>
    </div>
    <div class="header--spacer"></div>
    <div class="header--categories">
      <ul class="header--list">
        <li class="header--listitem">
          <nuxt-link to="/recruit">Recruit</nuxt-link>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;

  display: flex;
  align-items: center;

  height: 60px;
  width: 100vw;

  padding: 0 16px;

  background-color: rgba(0, 0, 0, 0.25);

  /* offset-x | offset-y | blur-radius | spread-radius | color */
  box-shadow: 0 2.5px 10px -2.5px black;

  /* Navigation's z-index: 20-30 */
  z-index: 20;

  &--logo {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  &--logo a {
    text-decoration: none;

    display: flex;
    align-items: center;
    justify-content: center;
  }

  &--spacer {
    flex: 1;
  }

  &--categories {
  }

  &--list {
    list-style: none;
    display: flex;
  }

  &--listitem {
    margin: 0 10px;
  }

  &--listitem a {
    text-decoration: none;
    color: white;
  }

  &--listitem a:hover,
  &--listitem a:active,
  &--listitem a.nuxt-link-active {
    color: red;
  }
}
</style>
