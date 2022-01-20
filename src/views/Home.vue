<template>
  <div class="container-fluid h-100">
    <div class="row mt-4 px-0 mx-auto">
      <div class="col-lg-12 col-md-12 col-sm-12 col-12">
        <b-form-input
          id="search"
          v-model="search"
          type="search"
          placeholder="Search"
        ></b-form-input>
      </div>
    </div>
    <div class="row">
      <div
        class="col-lg-3 col-md-3 col-sm-12 col-12 mt-5"
        v-for="(post, index) in filteredList"
        :key="index"
      >
        <div class="text-center border p-3">
          <img
            :src="post.img"
            :alt="post.title"
            width="100"
            height="100"
            class="object-fit"
          />
          <h3 class="mt-2">{{ post.title }}</h3>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Home",
  data() {
    return {
      search: "",
      postList: [
        {
          title: "Html-5",
          img: "https://www.w3.org/html/logo/downloads/HTML5_Logo_512.png",
        },
        {
          title: "CSS-3",
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS63s_TKNEbSDyCnpko2aIn2c4cCiuvh1chFaxyXPpChmvugRWHqyje2cMi-d0FuEYkYu8&usqp=CAU",
        },
        {
          title: "SASS",
          img: "https://miro.medium.com/max/600/1*wlQV5JRDIOlwqj1Ds8J4qQ.jpeg",
        },
        {
          title: "Boostrap",
          img: "https://getbootstrap.com/docs/4.5/assets/brand/bootstrap-social-logo.png",
        },
        {
          title: "JavaScript",
          img: "https://pluralsight2.imgix.net/paths/images/javascript-542e10ea6e.png",
        },
        {
          title: "Vue.js",
          img: "https://vuejs.org//images/logo.png",
        },
      ],
    };
  },
  computed: {
    filteredList() {
      return this.postList.filter((post) => {
        return post.title.toLowerCase().includes(this.search.toLowerCase());
      });
    },
  },
};
</script>