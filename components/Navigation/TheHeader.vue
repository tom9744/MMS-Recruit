<template>
  <header class="header">
    <div class="header--logo">
      <nuxt-link to="/">목멱성</nuxt-link>
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

  padding: 0 20px;

  background-color: rgba(0, 0, 0, 0.25);

  /* offset-x | offset-y | blur-radius | spread-radius | color */
  box-shadow: 0 2.5px 10px -2.5px black;

  /* Navigation's z-index: 20-30 */
  z-index: 20;

  &--logo {
    font-size: 1.5rem;
    font-weight: bold;
  }

  &--logo a {
    text-decoration: none;
    color: white;
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
