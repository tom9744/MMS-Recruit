<template>
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
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
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
