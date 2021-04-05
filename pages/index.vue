<template>
  <div class="container">
    <Carousel />

    <MainSection>
      <Content>
        <template #title>About</template>
        <template #subtitle>🤔 목멱성은 어떤 동아리인가요?</template>
        <template #paragraph>
          목멱성은 밴드 음악 동아리로 시작했지만, 악기를 배우고 싶거나 음악과
          관련된 컨텐츠에 관심이 있는 누구나 가입할 수 있습니다. 악기를 직접
          연주하지 않더라도 공연 영상 촬영/편집, 음원 프로듀싱 등 다양한 활동을
          경험해볼 수 있는 종합 음악 컨텐츠 제작 동아리입니다!
        </template>
      </Content>
    </MainSection>

    <MainSection>
      <Content>
        <template #title>Introduction</template>
        <template #subtitle>🎸 다양한 악기 및 음향장비 보유</template>
        <template #paragraph>
          목멱성은 밴드 음악뿐만 아니라 다양한 장르의 음악과 영상 편집 등 다양한
          분야를 포괄적으로 다루고 있습니다. 이에 필요한 다양한 악기와 음향
          장비를 자체 보유하고 있습니다.
        </template>
        <InstrumentList :instruments="instruments" />
      </Content>
    </MainSection>

    <MainSection>
      <Content>
        <template #title>Why MMS?</template>

        <AdvantageList :advantages="advantages" />
      </Content>
    </MainSection>

    <MainSection>
      <Content>
        <template #title>Activity</template>
        <template #subtitle>📆 목멱성은 어떤 활동을 하나요?</template>
        <template #paragraph>
          일 년 단위로 일정을 계획하고 있으며, 매년 최소 2회의 공연을 진행해
          왔습니다. 그 외에도 MT, 창립제, 체육대회를 진행하며, 소규모 비공식
          행사도 빈번히 발생(?)합니다. 또한 매주 화요일 6시 정기회의를 진행하고
          있습니다.
        </template>

        <ActivityList :activities="activities" />
      </Content>
    </MainSection>

    <MainSection>
      <Content>
        <template #title>Project</template>
        <template #subtitle> 🔥 활동 결과물을 확인해보세요!</template>
        <template #paragraph>
          목멱성은 매년 '학생회관 앞 공연', '6월 정기공연', '상시 외부공연' 등을
          통해 꾸준히 음악 활동을 하고 있습니다. 또한 공연 실황을 촬영 및
          편집하여 YouTube 채널에 업로드하고 있습니다.
        </template>
        <AppIframe
          source="https://www.youtube.com/embed/VoRaLXE5Dzw"
          :style="{ marginBottom: '8px' }"
        />
        <AppIframe source="https://www.youtube.com/embed/C-qG-qdpGh4" />
      </Content>
    </MainSection>

    <MainSection>
      <Content>
        <template #title>Contact</template>
        <template #subtitle>🤗 저희와 함께 하고 싶으신가요?</template>
        <template #paragraph>
          목멱성은 매학기 초(3월, 9월)에 신규부원 모집을 진행합니다. 하지만
          지정된 기간 이외에도 언제든 가입 신청이 가능합니다. 저희와 함께 하고
          싶으시다면, 아래의 채널 중 하나를 통해 문의해주세요!
        </template>

        <ContactList :contacts="contacts" />
      </Content>
    </MainSection>
  </div>
</template>

<script>
import Carousel from '~/components/Carousel/Carousel'
import MainSection from '~/components/Introduction/MainSection'
import Content from '~/components/Introduction/Content'
import InstrumentList from '~/components/Introduction/Instrument/InstrumentList'
import AdvantageList from '~/components/Introduction/Advantage/AdvantageList'
import ActivityList from '~/components/Introduction/Activity/ActivityList'
import AppIframe from '~/components/UI/AppIframe'
import ContactList from '~/components/Introduction/Contact/ContactList'

export default {
  components: {
    Carousel,
    MainSection,
    Content,
    InstrumentList,
    AdvantageList,
    AppIframe,
    ContactList,
    ActivityList,
  },

  data() {
    return {
      instruments: [
        { type: '기타', fileName: 'guitar.svg', soundFile: 'acoustic.wav' },
        {
          type: '전자기타',
          fileName: 'electric-guitar.svg',
          soundFile: 'electric.wav',
        },
        { type: '베이스', fileName: 'bass.svg', soundFile: 'bass.wav' },
        { type: '드럼', fileName: 'drums.svg', soundFile: 'drums.wav' },
        { type: '키보드', fileName: 'keyboard.svg', soundFile: 'keyboard.wav' },
      ],

      advantages: [
        {
          subject: '🍻 음주와 학업의 황금비율',
          description:
            '목멱성은 타의추종을 불허하는 술자리 문화를 가꿔오고 있습니다. 하지만 시험기간이 임박하면 개인 별 스터디를 진행하기도 하며, 학업에도 정성을 다하고 있습니다.',
        },
        {
          subject: '💞 활발한 선후배 커뮤니티',
          description:
            '1990년 창립된 목멱성은 자유로운 선후배 문화를 토대로 OB 네트워크를 쌓아오고 있습니다. 사회의 다양한 분야에 진출하여 활동하고 계신 선배님들로부터 조언을 구할 수 있습니다.',
        },
        {
          subject: '👨‍👩‍👧‍👦 다양한 학과 출신의 구성원',
          description:
            '과거에는 전자전기공학과/컴퓨터공학과 학생을 위주로 구성되어 왔습니다. 하지만 중앙 동아리로 전환하며, 공과대학을 넘어 더욱 다양한 학과의 학생들로 구성되게 되었습니다.',
        },
      ],

      contacts: [
        {
          link: 'https://www.facebook.com/groups/146570552120604',
          icon: {
            src: 'facebook.svg',
            alter: 'Facebook Icon',
            size: '32',
          },
        },
        {
          link: 'https://www.youtube.com/channel/UCW-Jungtim8fzkaC7uyjV4g',
          icon: {
            src: 'youtube.svg',
            alter: 'YouTube Icon',
            size: '32',
          },
        },
        {
          link: 'https://open.kakao.com/o/sQyQ8lUc',
          icon: {
            src: 'kakaotalk.svg',
            alter: 'KakaoTalk Icon',
            size: '32',
          },
        },
      ],

      activities: [
        {
          month: '3월',
          name: '학관 앞 공연',
          fileName: 'activity_1.jpeg',
          description: '학생회관 앞에서 대규모의 버스킹 공연을 진행합니다.',
        },
        {
          month: '4월',
          name: '정기 MT',
          fileName: 'activity_2.jpeg',
          description: '선후배, OB까지 함께하는 MT를 진행합니다.',
        },
        {
          month: '6월',
          name: '정기 공연',
          fileName: 'activity_3.jpeg',
          description: '목멱성의 1년 행사 중 가장 중요한 정기공연입니다.',
        },
        {
          month: '9월',
          name: '창립제, 체육대회',
          fileName: 'activity_4.jpeg',
          description: '목멱성 창립일을 기념하며, 체육대회를 진행합니다.',
        },
        {
          month: '상시',
          name: '외부 공연',
          fileName: 'activity_5.jpeg',
          description:
            '시기와 상관없이, 홍대/신촌 인근 클럽을 대관해 공연을 진행합니다.',
        },
      ],
    }
  },

  head() {
    return {
      title: '동국대학교 목멱성 | Home',

      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            '동국대학교 밴드 음악 동아리 목멱성 소개 페이지입니다. 목멱성의 연간 활동 일정과 연락처 등을 찾아볼 수 있습니다.',
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
          content: 'https://mms-dongguk.tk',
        },
        {
          hid: 'og:title',
          property: 'og:title',
          content: '동국대학교 목멱성',
        },
        {
          hid: 'og:description',
          property: 'og:description',
          content: '홈페이지 | 목멱성 동아리 소개',
        },
        {
          hid: 'og:image',
          property: 'og:image',
          content: 'https://mms-dongguk.tk/_nuxt/img/carousel_4.eaddd6e.jpeg',
        },
        {
          hid: 'og:image:alt',
          property: 'og:image:alt',
          content: '홈페이지 | 목멱성 동아리 소개',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped></style>
