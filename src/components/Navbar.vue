<template>
  <div class="container-fluid custom-navbar">
    <div class="row bg-color-white box-shadow">
      <div class="col-lg-12 col-md-12 col-sm-12 col-12 py-2">
        <div class="d-flex justify-content-between align-items-center">
          <div class="d-flex align-items-center">
            <img
              src="../assets/Images/bars-icon.png"
              alt="bars"
              width="20"
              class="mr-3 cursor-pointer"
              @click="$emit('toggle')"
            />
            <h3>Dashboard</h3>
          </div>
          <div
            class="
              search
              border-gray-1
              py-1
              px-1
              border-radius-18
              d-lg-block d-md-none d-sm-none d-none
            "
          >
            <img
              src="../assets/Images/search-icon.svg"
              alt="bars"
              width="18"
              class="mx-2 cursor-pointer"
            />
            <input type="text" placeholder="Search" />
          </div>
          <div>
            <div class="d-flex">
              <b-avatar variant="primary" text="JB"></b-avatar>
              <div>
                <h6 class="ml-2 mb-0">Jasmin Bhesaniya</h6>
                <h6 class="ml-2 color-light-gray font-size-14 mt-1">Admin</h6>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  emits: ["toggle"],
};
</script>
