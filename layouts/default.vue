<template>
  <div>
    <TheHeader />

    <Nuxt />

    <TheFooter />

    <TheScrollButton />
  </div>
</template>

<script>
import TheHeader from '~/components/Navigation/TheHeader'
import TheFooter from '~/components/Navigation/TheFooter'
import TheScrollButton from '~/components/Navigation/TheScrollButton'

export default {
  components: {
    TheHeader,
    TheFooter,
    TheScrollButton,
  },
}
</script>

<style lang="scss">
html {
  /* font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif; */
  font-family: 'Noto Sans KR', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
</style>
