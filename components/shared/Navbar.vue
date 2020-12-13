<template>
  <nav class="px-6">
    <div class="sm:flex sm:justify-between">
      <div class="flex justify-between items-center">
        <a href="#" class="text-6xl text-mainYellow">
          <fa
            class="bg-mainGrey px-1 rounded-t-full"
            :icon="['fab', 'angrycreative']"
          />
        </a>
        <!-- <a class="" href="index.html"><i class=""></i> DevCamper</a> -->
        <button
          class="text-4xl leading-none text-mainYellow focus:outline-none sm:hidden"
          @click="toogleNav = !toogleNav"
        >
          <fa v-if="toogleNav" :icon="['fas', 'bars']" />
          <fa v-else :icon="['fas', 'times']" />
        </button>
      </div>
      <div
        v-if="!toogleNav"
        class="text-2xl text-mainGrey sm:flex sm:items-center sm:px-4"
      >
        <ul class="sm:flex sm:justify-between sm:flex-row-reverse">
          <li class="nav-item py-3 sm:ml-4">
            <a class="nav-link" href="login.html"
              ><i class="fas fa-sign-in-alt"></i> Login</a
            >
          </li>
          <li class="nav-item py-3 sm:ml-4 nav-active">
            <a class="nav-link" href="register.html"
              ><i class="fas fa-user-plus"></i> Register</a
            >
          </li>
          <li class="nav-item py-3">
            <a class="nav-link" href="bootcamps.html">Browse Bootcamps</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  data() {
    return {
      toogleNav: false,
    };
  },
};
</script>
<style lang="scss" scoped>
.nav-active {
  border-bottom-width: 1.9px;
  border-color: $mainYellow;
  color: $navGray;
  a {
    cursor: default;
    color: $navGrayHover;
  }
}
.nav-item a {
  transition: 0.3s;
  &:hover {
    color: $navGrayHover;
  }
}
</style>
