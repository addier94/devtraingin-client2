<template>
  <div>
    <MainBanner />
    <!-- Latest bootcamps -->
    <div class="page-wrapper">
      <!-- <template v-if="$fetchState.pending && !articles.length">
      <div class="article-cards-wrapper">
        <content-placeholders
          v-for="p in 30"
          :key="p"
          rounded
          class="item"
        >
          <content-placeholders-img />
          <content-placeholders-text :lines="3" />
        </content-placeholders>
      </div>
    </template>
    <template v-else-if="$fetchState.error">
      <inline-error-block :error="$fetchState.error" />
    </template> -->
      <template>
        <div class="article-cards-wrapper">
          <item
            class="item"
            v-for="bootcamp in bootcamps[0].data"
            :key="bootcamp.id"
            :bootcamp="bootcamp"
          />
        </div>
      </template>
    </div>
  </div>
</template>

<script>
import Item from "@/components/shared/Item.vue";
export default {
  async fetch() {
    const bootcamps = await fetch(
      `https://bootcampapi.fernandezalfredo.com/api/v1/bootcamps`
    ).then((res) => res.json());
    this.bootcamps = this.bootcamps.concat(bootcamps);
  },
  data() {
    return {
      bootcamps: [],
    };
  },
  head() {
    return {
      title: "All bootcamps",
    };
  },
};
</script>


<style lang="scss" scoped>
.page-wrapper {
  @apply max-w-screen-xl m-auto p-4 min-h-screen;
}
.article-cards-wrapper {
  @apply flex flex-wrap items-start;
  .item {
    width: calc(100% - 2 * 0.5rem);
    margin: 0.5rem;
    @media (min-width: 640px) {
      width: calc(50% - 2 * 0.5rem);
    }
    @media (min-width: 1024px) {
      width: calc(33.33333% - 2 * 0.5rem);
    }
  }
}
</style>
