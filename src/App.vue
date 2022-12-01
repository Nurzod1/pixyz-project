<template>
  <div id="app">
    <component :is="currentLayout" />
  </div>
</template>

<script>
import MainLayout from "@/layout/MainLayout";

export default {
  components: {
    MainLayout,
  },
  computed: {
    currentLayout() {
      switch (this.$route.meta.layout) {
        case "main":
          return "main-layout";
      }
    },
  },
};
</script>

<style lang="scss">
@import "@/assets/scss/main.scss";

#app {
  font-size: 16px;
}
</style>
