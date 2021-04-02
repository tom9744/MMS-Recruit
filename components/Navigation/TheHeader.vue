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

  height: 60px;
  width: 100vw;

  padding: 0 20px;

  display: flex;
  align-items: center;

  &--logo {
    font-size: 1.5rem;
  }

  &--logo a {
    text-decoration: none;
    color: black;
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
    color: black;
  }

  &--listitem a:hover,
  &--listitem a:active,
  &--listitem a.nuxt-link-active {
    color: red;
  }
}
</style>
