<template>
  <div class="main">
    <div class="main-content">
      <h1>Welcome to Beijing</h1>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HomeMain'
  }
</script>

<style scoped lang="scss">
  @import "../../assets/scss/common";

  .main {
    @include whall;

    .main-content {
      @include whall;
      display: flex;
      justify-content: center;

      h1 {
        font-size: 36px;
        margin-top: 20%;
      }
    }
  }
</style>
