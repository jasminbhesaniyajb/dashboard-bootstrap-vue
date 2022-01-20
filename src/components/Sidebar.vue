<template>
  <div
    class="
      pt-2
      px-2
      h-100
      responsive-sidebar
      custom-sidebar
      box-shadow
      bg-color-blue
    "
    :class="show ? 'w-1' : 'w-3'"
  >
    <div class="d-flex align-items-center">
      <h2
        :class="
          sideBarHide ? 'ml-2 color-white' : 'font-size-20 color-white mx-auto'
        "
      >
        Admin
      </h2>
    </div>
    <div :class="sideBarHide ? 'pl-1 pt-4' : 'ml-0 pt-4'">
      <router-link to="/" class="custom-link">
        <div class="d-flex align-items-center cursor-pointer my-2 p-2">
          <img
            src="../assets/Images/home-icon.svg"
            alt=""
            width="30"
            :class="sideBarHide ? '' : 'mx-auto'"
          />
          <h5 :class="sideBarHide ? 'ml-2 color-white mb-0' : ' d-none'">
            Home
          </h5>
        </div>
      </router-link>
      <router-link to="/about" class="custom-link">
        <div
          class="d-flex align-items-center cursor-pointer my-2 custom-link p-2"
        >
          <img
            src="../assets/Images/teachers-white.svg"
            alt=""
            width="30"
            :class="sideBarHide ? '' : 'mx-auto'"
          />
          <h5 :class="sideBarHide ? 'ml-2 color-white mb-0' : 'd-none'">
            Customer
          </h5>
        </div>
      </router-link>
      <div
        class="d-flex align-items-center cursor-pointer my-2 custom-link p-2"
      >
        <img
          src="../assets/Images/shopping-cart.svg"
          alt=""
          width="30"
          :class="sideBarHide ? '' : 'mx-auto'"
        />
        <h5 :class="sideBarHide ? 'ml-2 color-white mb-0' : 'd-none'">Order</h5>
      </div>
      <div
        class="d-flex align-items-center cursor-pointer my-2 custom-link p-2"
      >
        <img
          src="../assets/Images/master.svg"
          alt=""
          width="30"
          :class="sideBarHide ? '' : 'mx-auto'"
        />
        <h5 :class="sideBarHide ? 'ml-2 color-white mb-0' : 'd-none'">Task</h5>
      </div>
      <div
        class="d-flex align-items-center cursor-pointer my-2 custom-link p-2"
      >
        <img
          src="../assets/Images/settings.svg"
          alt=""
          width="30"
          :class="sideBarHide ? '' : 'mx-auto'"
        />
        <h5 :class="sideBarHide ? 'ml-2 color-white mb-0' : 'd-none'">Settings</h5>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  props: {
    sideBarHide: {
      type: Boolean,
    },
    show: {
      type: Boolean,
    },
  },
};
</script>

<style></style>
