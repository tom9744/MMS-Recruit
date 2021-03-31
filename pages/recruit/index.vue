<template>
  <div class="container">
    <section class="banner">
      <h1 class="banner--text">Recruit</h1>
    </section>

    <article class="notice">
      <h2 class="notice--title">😢 지금은 모집기간이 아니에요.</h2>

      <p class="notice--paragraph">
        하지만 실망하지마세요! 상시 지원도 가능합니다.
      </p>
    </article>

    <article class="recruit">
      <h2 class="recruit--title">지원 안내</h2>

      <ul class="recruit--list detail">
        <li class="recruit--listitem detail--card">
          <h3 class="detail--title">모집 일정</h3>

          <p class="detail--paragraph">
            매 학기 시작과 함께 신규 모집을 진행합니다. 기간 외에도 항상 상시
            지원이 가능하며, 이 경우 집행부원에게 직접 문의해주시기 바랍니다.
          </p>
        </li>

        <li class="recruit--listitem detail--card">
          <h3 class="detail--title">지원 자격</h3>

          <ul class="detail--list">
            <li class="talent">밴드 음악, 악기에 관심이 있는 누구나!</li>
            <li class="talent">영상 제작, 믹싱에 관심있는 누구나!</li>
          </ul>

          <em class="detail--emphasize">학번, 나이 제한 전혀 없습니다.</em>
        </li>

        <li class="recruit--listitem detail--card">
          <h3 class="detail--title">모집 분야</h3>

          <ul class="detail--list">
            <li class="department">[밴드] 보컬/기타/베이스/드럼/키보드</li>
            <li class="department">[영상] 영상 편집</li>
            <li class="department">[음향] 녹음/프로듀싱</li>
          </ul>

          <em class="detail--emphasize">로직, 파이널컷 가능자 우대</em>
        </li>
      </ul>
    </article>

    <article class="application">
      <h1 class="application--title">지원하기</h1>

      <p class="application--paragraph">
        아래 버튼을 눌러 지원서 작성을 시작해주세요.
      </p>

      <button class="application--button">지원하기</button>
    </article>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.container {
  width: 100vw;

  padding: 0 5%;
}

.banner {
  height: 15vh;
  width: 100%;

  display: flex;
  align-items: center;

  &--text {
  }
}

.notice {
  width: 100%;

  padding: 5% 0;

  box-sizing: border-box;

  &--title {
    margin-bottom: 2rem;
  }
  &--body {
  }
  &--subtitle {
    margin-bottom: 1rem;
  }
  &--paragraph {
  }
}

.recruit {
  width: 100%;

  padding: 5% 0;

  box-sizing: border-box;

  &--title {
    margin-bottom: 2rem;
  }
  &--list {
    list-style: none;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    padding: 0;
  }
  &--listitem {
  }
}

.detail {
  &--card {
    width: 100%;

    margin: 0.5rem;
    padding: 10%;

    border-radius: 1rem;

    background-color: white;
  }

  &--title {
    margin-bottom: 1rem;
  }

  &--list {
    list-style: none;

    padding: 0;
  }

  &--listitem {
  }

  &--paragraph {
  }

  &--emphasize {
    font-size: 0.75rem;
  }
}

.talent,
.department {
  margin-bottom: 0.5rem;
}

.application {
  width: 100%;

  padding: 5% 0;

  box-sizing: border-box;

  &--title {
    margin-bottom: 2rem;
  }
  &--paragraph {
    margin-bottom: 1rem;
  }
  &--button {
    text-decoration: none;
    border: none;

    height: 32px;
    width: 100%;

    background-color: lightgreen;

    margin: auto;
  }
}

@media screen and (min-width: 780px) {
  .container {
    padding: 0 15%;
  }

  .recruit {
    &--list {
      flex-direction: row;
    }
  }

  .detail {
    &--card {
      height: 220px;

      flex: 1;

      margin: 0.5rem;
      padding: 2.5%;

      border-radius: 1rem;

      background-color: white;
    }

    &--title {
      margin-bottom: 1rem;
    }

    &--list {
      list-style: none;

      padding: 0;
    }

    &--listitem {
    }

    &--paragraph {
    }

    &--emphasize {
      font-size: 0.75rem;
    }
  }
}
</style>
