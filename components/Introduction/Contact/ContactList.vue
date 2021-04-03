<template>
  <ul class="contact">
    <li v-for="(contact, idx) of contacts" :key="idx" class="contact--listitem">
      <a class="contact--link" :href="contact.link" target="_blank">
        <AppIcon
          class="contact--icon"
          :source="contact.icon.src"
          :alter="contact.icon.alter"
          :size="+contact.icon.size"
        />
      </a>
    </li>
  </ul>
</template>

<script>
import AppIcon from '~/components/UI/AppIcon'

export default {
  components: {
    AppIcon,
  },

  props: {
    contacts: {
      type: Array,
      requried: true,
      default() {
        return []
      },
    },
  },
}
</script>

<style lang="scss" scoped>
.contact {
  list-style: none;

  display: flex;
  align-items: flex-end;
  justify-content: space-around;
  flex-wrap: nowrap;

  height: 100px;
  width: 100%;

  &--listitem {
    height: 50px;
    width: 50px;

    padding: 0.5rem;

    background-color: white;
    border-radius: 50%;
  }

  &--link {
    display: flex;
    align-items: center;
    justify-content: center;

    height: 100%;
    width: 100%;
  }

  &--icon {
    height: 25px;
    width: 25px;
  }
}

@media screen and (min-width: 400px) {
  .contact {
    height: 175px;

    &--listitem {
      height: 70px;
      width: 70px;
    }

    &--icon {
      height: 35px;
      width: 35px;
    }
  }
}

@media screen and (min-width: 780px) {
  .contact {
    height: 200px;

    &--listitem {
      height: 80px;
      width: 80px;
    }

    &--icon {
      height: 40px;
      width: 40px;
    }
  }
}

@media screen and (min-width: 1080px) {
  .contact {
    height: 225px;

    &--listitem {
      height: 90px;
      width: 90px;
    }

    &--icon {
      height: 45px;
      width: 45px;
    }
  }
}
</style>
