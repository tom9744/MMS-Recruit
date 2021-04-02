<template>
  <div>
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

    <Nuxt />

    <footer class="footer">
      <ul class="footer--author">
        <li class="footer--author-info">
          <strong>Developer</strong> Junyoung Yang
        </li>
        <li class="footer--author-info">
          <strong>Report</strong>
          <a
            href="mailto:catfishdev9601@gmail.com?subject=[목멱성 소개페이지] 버그 리포트입니다."
            target="_blank"
            >버그 리포트 작성</a
          >
        </li>
        <li class="footer--author-info">
          <strong>Open Source</strong>
          <a href="https://github.com/tom9744/MMS-Recruit" target="_blank"
            >Github Repository</a
          >
        </li>
      </ul>

      <div class="footer--copyright">
        <p><strong>Copyright</strong> © Junyoung Yang 2021.</p>
        <p>All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

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

.footer {
  height: 200px;
  width: 100vw;

  padding: 0 20px;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;

  &--author {
    list-style: none;
  }

  &--author a {
    text-decoration: none;
    color: black;
  }

  &--copyright {
    text-align: center;
  }
}

@media screen and (min-width: 780px) {
  .footer {
    flex-direction: row;
  }
}
</style>
