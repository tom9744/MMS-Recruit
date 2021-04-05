<template>
  <footer class="footer">
    <Author class="footer--column" :author-info="authorInfo" />

    <License class="footer--column">
      <template #category>Copyright</template>

      ©
      <AppAnchor
        href="https://github.com/tom9744"
        title="Junyoung Yang"
        relation="author"
      />
      2021. All rights reserved.
    </License>

    <License class="footer--column">
      <template #category>Icons</template>

      made by
      <AppAnchor
        href="https://www.flaticon.com/authors/pixel-perfect"
        title="Pixel perfect"
        relation="license"
      />
      and
      <AppAnchor
        href="https://www.freepik.com"
        title="Freepik"
        relation="license"
      />
      from
      <AppAnchor
        href="https://www.flaticon.com"
        title="Flaticon"
        relation="license"
      />
    </License>
  </footer>
</template>

<script>
import Author from '~/components/Navigation/TheFooter/Auhtor'
import License from '~/components/Navigation/TheFooter/License'
import AppAnchor from '~/components/UI/AppAnchor'

export default {
  components: {
    Author,
    License,
    AppAnchor,
  },

  data() {
    return {
      authorInfo: [
        { category: 'Developer', text: 'Junyoung Yang', link: null },
        {
          category: 'Report',
          text: null,
          link: {
            href: 'mailto:catfishdev9601@gmail.com',
            title: '버그 리포트 (Gmail)',
          },
        },
        {
          category: 'Open Source',
          text: null,
          link: {
            href: 'https://github.com/tom9744/MMS-Recruit',
            title: 'Github Repository',
          },
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.footer {
  min-height: 150px;
  width: 100%;

  padding: 0 10%;

  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-around;

  font-size: 0.85rem;

  &--column {
    margin: 1rem 0;
  }
}

@media screen and (min-width: 780px) {
  .footer {
    flex-direction: row;
    align-items: center;

    &--column {
      flex: 1;

      margin: 0;
      padding: 0 1rem;
    }
  }
}
</style>
