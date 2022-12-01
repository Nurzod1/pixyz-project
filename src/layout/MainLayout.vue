<template>
  <div class="main-layout">
    <div class="layout-content">
      <div class="sidebar-wrapper">
        <sidebar :active="isActive" @close="isActive = false"/>
      </div>
      <Navbar @isOpen="isActive = true" />
      <router-view />
      <Footer />
      <SubFooter />
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import Footer from "@/components/Footer.vue";
import SubFooter from "../components/SubFooter.vue";
import Sidebar from '../components/Sidebar.vue';

export default {
  components: {
    Navbar,
    Footer,
    SubFooter,
    Sidebar,
  },

  data() {
    return {
      isActive: false,
    };
  },
};
</script>

<style></style>
