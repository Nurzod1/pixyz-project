<template>
  <div class="sidebar-parent">
    <div
      :class="['sidebar-overlay', { open: active }]"
      @click="$emit('close')"
    ></div>
    <div :class="['sidebar', { open: active }]">
      <div class="wrapper">
        <div class="sidebar-menu-wrapper">
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
  </div>
</template>

<script>
import LangSwitcher from "@/components/navbar/langSwitcher"

export default {
  name: "Sidebar",
  components: { LangSwitcher },
  data() {
    return {
      categoryStatus: false,
      subjectStatus: false,
      ageStatus: false,

      ex4: ["success", "success", "success"],

      models: {
        base: false,
        conditional: false,
      },
    };
  },
  props: {
    active: {
      type: Boolean,
    },
  },
};
</script>

<style lang="scss" scoped>
.sidebar-parent {
  position: relative;
  z-index: 9999999;
}

.sidebar-overlay {
  display: none;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
  &.open {
    display: block;
  }
}
.sidebar {
  position: fixed;
  width: 70vw;
  min-height: 100vh;
  right: 0;
  background: #ffffff;
  transform: translateX(100%);
  transition: all 0.4s;
  box-shadow: 0px 0px 30px rgba(0, 0 ,0 , 0.3);
  z-index: 2222222;

  &.open {
    right: 0;
    transform: translateX(0%);
  }

  @include breakpoint(md) {
    display: block;
  }

  .wrapper {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100vh;
    position: relative;
  }

  &-menu-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: auto;
  }

  .filter-price {
    display: flex;
    flex-direction: column;
    border-bottom: 1px solid #e0e0e0;

    &-icon {
      padding: 7px 16px 7px 16px;
    }

    &-body {
      p {
        font-family: "Lato";
        font-size: 15px;
        line-height: 17px;
        padding: 10px 5px 10px 11px;
        margin: 0;
        color: #414141;
        border-bottom: 1px solid #e0e0e0;

        &:first-child {
          border-top: 1px solid #e0e0e0;
        }
      }
    }

    &.open {
      .filter-price-body {
        display: block;
      }

      .filter-price-icon {
        svg {
          transform: rotate(180deg);
        }
      }
    }
  }

  .filter-price-icon {
    display: flex;
    align-items: center;
    justify-content: space-between;
    transition: all 0.3s;
    gap: 5px;

    .sidebar-button {
      font-family: "Lato";
      font-size: 15px;
      line-height: 27px;
      text-transform: capitalize;
      color: #1d1d1d;
      text-decoration: none;
    }
  }

  .filter-price-body {
    display: none;
    transition: all 0.3s;
  }

  .close-icon {
    position: absolute;
    right: 5px;
    top: 0px;
  }

  .menu-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
    padding-top: 30px;
  }
  .menu {
    font-family: "Seg";
    font-size: 15px;
    color: #000000;
    text-align: center;
    text-decoration: none;
  }
}
</style>
