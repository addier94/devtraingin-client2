<template>
  <section class="banner-container flex items-end">
    <div class="px-4 py-2">
      <h1 class="fff-calligraffitti text-3xl">Find a Code Bootcamp</h1>
      <p class="font-bold text-3xl uppercase">
        Find, rate and read reviews on coding bootcamps
      </p>
      <form class="w-full sm:w-9/12 md:w-3/6">
        <div class="grid grid-cols-2 gap-4">
          <div class="mb-2">
            <!-- <input type="text" name="zipcode" placeholder="Enter Zipcode" /> -->
            <input
              type="text"
              class="py-2 px-3 focus:outline-none w-full"
              placeholder="Miles From"
            />
          </div>
          <div class="mb-2">
            <input
              type="text"
              class="py-2 px-3 focus:outline-none w-full"
              placeholder="Enter Zipcode"
            />
          </div>
        </div>
        <input
          class="btn btn-yellow w-full"
          type="submit"
          value="Find Bootcamps"
        />
      </form>
    </div>
  </section>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.banner-container {
  background: url("~assets/images/bannerbcg.jpeg");
  min-height: calc(100vh - 6rem);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
}
</style>
