<template>
  <div class="language">
    <div class="language-wrapper" @click="isOpen = !isOpen">
      <div class="language__title">
        {{ currentLang.label }}
      </div>
      <div :class="['language__icon', { open: isOpen }]">
        <svg
          width="17"
          height="9"
          viewBox="0 0 17 9"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M0.5 0.5L8.5 8.5" stroke="black" stroke-linecap="round" />
          <path d="M16.5 0.5L8.5 8.5" stroke="black" stroke-linecap="round" />
        </svg>
      </div>
    </div>

    <div :class="['language-menu', { active: isOpen }]">
      <div
        v-for="lang in languages"
        :key="lang.code"
        :class="[
          'language-menu__item',
          { active: lang.code === currentLang.code },
        ]"
        @click="changeLang(lang)"
      >
        {{ lang.label }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "language-switcher",
  data() {
    return {
      isOpen: false,
      currentLang: {
        code: "ru",
        label: "Ru",
      },
      languages: [
        {
          code: "uz",
          label: "Uz",
        },
        {
          code: "ru",
          label: "Ru",
        },
      ],
    };
  },
  methods: {
    changeLang(lang) {
        this.currentLang = lang;
        this.isOpen = false;
    }
  }
};
</script>

<style lang="scss">
.language {
  position: relative;

  &-wrapper {
    display: flex;
    align-items: center;
    border-radius: 6px;
    border: 1px solid #efefef;
    padding: 5px 8px;
    cursor: pointer;
  }

  &__title {
    font-family: "Seg-bold";
    margin-right: 10px;
  }

  &__icon {
    width: 15px;
    height: 15px;
    transition: 0.3s;

    &.open {
      transform: rotate(180deg);
    }

    svg {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }

  &-menu {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    display: flex;
    flex-direction: column;
    border: 1px solid #efefef;
    border-radius: 6px;
    transition: 0.5s;
    opacity: 0;
    pointer-events: none;

    &.active {
      transform: translateY(10px);
      opacity: 1;
      pointer-events: unset;
    }

    &__item {
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 5px;
      color: #000;
      transition: 0.4s;
      cursor: pointer;

      &.active {
        background: rgba(94, 193, 223, 0.918);
        color: #fff;
      }
    }
  }
}
</style>
