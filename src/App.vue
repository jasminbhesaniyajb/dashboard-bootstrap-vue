<template>
  <div class="d-lg-flex d-md-flex">
    <div :class="show ? 'w-1' : 'w-3'">
      <Sidebar :sideBarHide="sideBarHide" :show="show" />
    </div>
    <div :class="show ? 'w-99' : 'w-97'">
      <Navbar @toggle="toggle" />
      <router-view />
    </div>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Sidebar from "./components/Sidebar.vue";
export default {
  name: "App",
  components: {
    Navbar,
    Sidebar,
  },
  data() {
    return {
      show: false,
      sideBarHide: true,
    };
  },
  methods: {
    toggle() {
      this.show = !this.show;
      this.sideBarHide = !this.sideBarHide;
      console.log("hello");
    },
  },
};
</script>

<style lang="scss">
@import "~@/assets/scss/vendors/bootstrap-vue/index";
</style>
