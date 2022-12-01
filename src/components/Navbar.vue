<template>
  <div :class="[{ change_color: scrollPosition > 50 }, 'navbar']">
    <div class="container">
      <div class="navbar-wrapper">
        <div class="burger-wrapper" @click="$emit('isOpen')">
          <svg
            width="28"
            height="15"
            viewBox="0 0 28 17"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M1.4 2.83333H26.6C26.9713 2.83333 27.3274 2.68408 27.59 2.4184C27.8525 2.15272 28 1.79239 28 1.41667C28 1.04094 27.8525 0.680609 27.59 0.414932C27.3274 0.149256 26.9713 0 26.6 0H1.4C1.0287 0 0.672601 0.149256 0.41005 0.414932C0.1475 0.680609 0 1.04094 0 1.41667C0 1.79239 0.1475 2.15272 0.41005 2.4184C0.672601 2.68408 1.0287 2.83333 1.4 2.83333V2.83333ZM26.6 14.1667H1.4C1.0287 14.1667 0.672601 14.3159 0.41005 14.5816C0.1475 14.8473 0 15.2076 0 15.5833C0 15.9591 0.1475 16.3194 0.41005 16.5851C0.672601 16.8507 1.0287 17 1.4 17H26.6C26.9713 17 27.3274 16.8507 27.59 16.5851C27.8525 16.3194 28 15.9591 28 15.5833C28 15.2076 27.8525 14.8473 27.59 14.5816C27.3274 14.3159 26.9713 14.1667 26.6 14.1667ZM26.6 7.08333H1.4C1.0287 7.08333 0.672601 7.23259 0.41005 7.49827C0.1475 7.76394 0 8.12428 0 8.5C0 8.87572 0.1475 9.23606 0.41005 9.50173C0.672601 9.76741 1.0287 9.91667 1.4 9.91667H26.6C26.9713 9.91667 27.3274 9.76741 27.59 9.50173C27.8525 9.23606 28 8.87572 28 8.5C28 8.12428 27.8525 7.76394 27.59 7.49827C27.3274 7.23259 26.9713 7.08333 26.6 7.08333Z"
              fill="#1A4900"
            />
          </svg>
        </div>
        <div class="logo-wrapper">
          <img @click="$router.push('/')" src="@/assets/img/logo.png" alt="" />
        </div>
        <div class="menu-wrapper">
          <router-link class="menu" to="/" exact-active-class="active">
            HOME
          </router-link>

          <router-link class="menu" to="/about" exact-active-class="active">
            ABOUT US
          </router-link>

          <router-link class="menu" to="/services" exact-active-class="active">
            SERVICES
          </router-link>

          <router-link class="menu" to="/portfolio" exact-active-class="active">
            PORTFOLIO
          </router-link>

          <router-link class="menu" to="/contact" exact-active-class="active">
            CONTACT
          </router-link>
        
          <lang-switcher />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import LangSwitcher from "@/components/navbar/langSwitcher"

export default {
  name: "navbar",
  components: { LangSwitcher },
  data() {
    return {
      scrollPosition: null,
      open: false,
    };
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY;
    },
  },
  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.updateScroll);
  },
};
</script>

<style lang="scss" scoped>
.navbar {
  position: fixed;
  right: 0;
  left: 0;
  background: transparent;
  z-index: 11111;

  &.change_color {
    box-shadow: 0 0 10px #aaa;
    background: #ffffff;
  }

  &-wrapper {
    display: flex;
    justify-content: space-between;
    padding: 0 15px;

    @include breakpoint(md) {
      flex-direction: row-reverse;
    }
  }

  .burger-wrapper {
    display: none;

    @include breakpoint(md) {
      display: block;
    }
  }

  .logo-wrapper {
    padding: 10px 0;
    height: 70px;
    cursor: pointer;

    img {
      width: 100%;
      height: 100%;
      object-fit: contain;  
    }
  }

  .menu-wrapper {
    display: flex;
    gap: 52px;

    @include breakpoint(md) {
      display: none;
    }
  }
  .menu {
    display: flex;
    align-items: center;
    font-family: "Seg-bold";
    font-size: 15px;
    color: #000000;
    text-align: center;
    text-decoration: none;
    position: relative;

    &::before {
      display: block;
      content: attr(title);
      font-weight: bold;
      height: 0;
      overflow: hidden;
      visibility: hidden;
    }

    &:hover {
      color: #49d6cb;
      transition: all 0.3s;
    }

    &::after {
      content: "";
      position: absolute;
      right: 50%;
      left: 50%;
      bottom: 0;
      height: 3px;
      background-color: #49d6cb;
      transition: all 0.3s;
    }

    &:hover::after {
      right: -40%;
      left: -40%;
      transition: all 0.3s;
    }

    &.active {
      font-family: "Seg-bold";
      color: #49d6cb;
    }
  }

  .language {
    display: flex;
    align-items: center;
    gap: 4.5px;
    p {
      font-family: "Seg";
      font-size: 15px;
      line-height: 17px;
      color: #000000;
    }
  }
}
</style>
