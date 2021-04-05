<template>
  <div class="container">
    <section class="banner">
      <h1 class="banner--text">Recruit</h1>
    </section>

    <RecruitArticle>
      <template #title>😢 지금은 모집기간이 아니에요.</template>
      <template #content>
        <p>다음 신규회원 모집은 2학기 시작과 함께, 9월경 진행될 예정입니다.</p>
      </template>
    </RecruitArticle>

    <RecruitArticle>
      <template #title>지원 안내</template>
      <template #content>
        <InfoList :informations="informations"> </InfoList>
      </template>
    </RecruitArticle>

    <RecruitArticle>
      <template #title>지원하기</template>
      <template #content>
        <p :style="{ marginBottom: '1.5rem' }">
          아래 버튼을 눌러 지원서 작성을 시작해주세요.
        </p>

        <RecruitButton>지원서 작성</RecruitButton>
      </template>
    </RecruitArticle>
  </div>
</template>

<script>
import RecruitArticle from '~/components/Recruit/UI/RecruitArticle'
import RecruitButton from '~/components/Recruit/UI/RecruitButton'
import InfoList from '~/components/Recruit/InfoList'

export default {
  components: {
    RecruitArticle,
    RecruitButton,
    InfoList,
  },

  data() {
    return {
      informations: [
        {
          title: '📆 모집 일정',
          para:
            '매 학기 시작과 함께 신규 모집을 진행합니다. 기간 외에도 항상 상시 지원이 가능하며, 이 경우 집행부원에게 직접 문의해주시기 바랍니다.',
          list: null,
          emphasize: null,
        },
        {
          title: '💁‍♂️ 지원 자격',
          para: null,
          list: [
            '밴드 음악, 악기에 관심이 있는 누구나!',
            '영상 제작, 믹싱에 관심있는 누구나!',
          ],
          emphasize: '학번, 나이 제한 없습니다.',
        },
        {
          title: '🎤 모집 분야',
          para: null,
          list: [
            '[밴드] 보컬/기타/베이스/드럼/키보드',
            '[영상] 영상 편집',
            '[음향] 녹음/프로듀싱',
          ],
          emphasize: '로직, 파이널컷 가능자 우대',
        },
      ],
    }
  },

  head() {
    return {
      title: '동국대학교 목멱성 | Recruit',

      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            '동국대학교 밴드 음악 동아리 목멱성 신규회원 모집 전용 페이지입니다. 신규 회원 모집과 관련된 모든 정보를 얻을 수 있습니다.',
        },
        // SNS 공유 미리보기 관련 설정
        {
          hid: 'og:type',
          property: 'og:type',
          content: 'website',
        },
        {
          hid: 'og:url',
          property: 'og:url',
          content: 'https://mms-dongguk.tk/recruit',
        },
        {
          hid: 'og:title',
          property: 'og:title',
          content: '동국대학교 목멱성',
        },
        {
          hid: 'og:description',
          property: 'og:description',
          content: '가입신청 | 목멱성 신규부원 모집 안내 및 지원',
        },
        {
          hid: 'og:image',
          property: 'og:image',
          content: 'https://mms-dongguk.tk/_nuxt/img/carousel_4.eaddd6e.jpeg',
        },
        {
          hid: 'og:image:alt',
          property: 'og:image:alt',
          content: '가입신청 | 목멱성 신규부원 모집 안내 및 지원',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.container {
  width: 100vw;

  margin: 60px 0;
  padding: 0 5%;
}

.banner {
  height: 15vh;
  width: 100%;

  display: flex;
  align-items: center;
}

@media screen and (min-width: 780px) {
  .container {
    padding: 0 15%;
  }
}

@media screen and (min-width: 1080px) {
  .container {
    padding: 0 25%;
  }
}
</style>
