<template>
  <nav class="bg-gray-400 px-6 py-4">
    <div class="flex justify-between">
      <fa class="text-6xl" :icon="['fab', 'angrycreative']" />
      <!-- <a class="" href="index.html"><i class=""></i> DevCamper</a> -->
      <button class="" type="button">
        <fa class="text-4xl" :icon="['fas', 'bars']" />
      </button>
    </div>
    <div class="">
      <ul class="">
        <li class="nav-item">
          <a class="nav-link" href="login.html"
            ><i class="fas fa-sign-in-alt"></i> Login</a
          >
        </li>
        <li class="nav-item">
          <a class="nav-link" href="register.html"
            ><i class="fas fa-user-plus"></i> Register</a
          >
        </li>
        <li class="nav-item">
          <a class="nav-link" href="bootcamps.html">Browse Bootcamps</a>
        </li>
      </ul>
    </div>
  </nav>
</template>
<style lang="scss" scoped>
</style>
