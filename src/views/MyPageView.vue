<script setup>
// example components
import DefaultNavbar from "../examples/navbars/NavbarDefault.vue";
import Header from "../examples/Header.vue";
import DefaultFooter from "../examples/footers/FooterDefault.vue";

// sections
import Profile from "../components/MyPageSections/AuthorProfile.vue";
import Posts from "../components/MyPageSections/AuthorPosts.vue";

// image
import image from "@/assets/img/city-profile.jpg";
</script>
<template>
  <DefaultNavbar transparent />
  <Header class="no-select">
    <div
      class="page-header min-height-400"
      :style="{ backgroundImage: `url(${image})` }"
      loading="lazy"
    >
      <span class="mask bg-gradient-dark opacity-8"></span>
    </div>
  </Header>
  <div class="card card-body blur shadow-blur mx-3 mx-md-4 mt-n6 mb-4 no-select">
    <Profile />
    <Posts />
  </div>
  <DefaultFooter />
</template>

<style>
.no-select {
  user-select: none;
  -webkit-user-drag: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
}
</style>
