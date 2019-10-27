<template>
  <div class="project">
    <nuxt/>
  </div>
</template>

<style lang="scss">
  @import "../assets/scss/common";

  #__nuxt {
    @include whall;

    #__layout {
      @include whall;

      .project {
        @include whall;
      }
    }
  }
</style>
