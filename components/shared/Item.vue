<template>
  <article>
    <nuxt-link to="/" class="image-wrapper cursor-pointer" tag="div">
      <div class="absolute top-0 right-0 z-10 text-white">
        <div class="time-publish-post">
          <span class="font-medium">{{
            $moment(bootcamp.createdAt, "YYYYMMDD").fromNow()
          }}</span>
          <span class="font-bold tracking-tighter">{{
            $moment(bootcamp.createdAt).format("L")
          }}</span>
        </div>
      </div>
      <img
        src="https://miro.medium.com/max/1200/1*mk1-6aYaf_Bes1E3Imhc0A.jpeg"
      />
      <!-- <img src="article.social_image" :alt="article.title" /> -->
    </nuxt-link>
    <div class="content">
      <div class="meta text-xs flex items-center mb-2">
        <a class="mr-1">
          <img
            class="rounded-full w-10"
            src="https://cdn.pixabay.com/photo/2017/06/13/12/53/profile-2398782_1280.png"
          />
        </a>
        <div>
          <a class="user-name text-base">alredo fernandez</a>
          <div class="scl flex">
            <span class="flex items-center mr-4">
              <heart-icon />
              88
            </span>
            <span class="flex items-center mr-4">
              <comments-icon />
              849
            </span>
          </div>
        </div>
      </div>
      <a>
        <h1>reunion de profesores</h1>
      </a>
      <div class="tags">
        <a class="tag"> tag linux medium </a>
      </div>
    </div>
  </article>
</template>

<script>
export default {
  props: ["bootcamp"],
};
</script>


<style lang="scss" scoped>
article {
  border-radius: 1rem;
  overflow: hidden;
  // box-shadow: $shadow;
  &:hover {
    // box-shadow: $small-shadow;
    h1 {
      transition: all 0.2s ease;
      &:hover {
        // color: $primary-color;
      }
    }
  }
  .user-name {
    transition: all 0.2s ease;
    &:hover {
      // color: $primary-color;
    }
  }
  .time-publish-post {
    background: $navGrayHover;
    min-width: 70px;
    border-radius: 0 10px 0 90%;
    padding: 8px 0 28px;
    display: inline-flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    line-height: 1rem;
    span:nth-child(odd) {
      font-size: 0.6rem;
    }
    span:nth-child(2n) {
      font-size: 1rem;
    }
  }
  .image-wrapper {
    position: relative;
    padding-bottom: 56.25%;
    // background-color: $elevated-surface-color;
    background: green;
    img {
      @apply absolute top-0 left-0 w-full h-full object-cover;
    }
  }
  .content {
    padding: 1rem;
    h1 {
      font-size: 2rem;
      // font-size: $text-xl;
      // letter-spacing: $-ls2;
      margin-bottom: 0.5rem;
    }
  }
}
</style>
