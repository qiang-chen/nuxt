<template>
  <div class="container"></div>
</template>

<script>
  export default {
    mounted () {
      this.$router.push('/login')
    }
  }
</script>

<style lang="scss" scoped>
  @import "../assets/scss/common";

  .container {
    @include whall;
  }
</style>
