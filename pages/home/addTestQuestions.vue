<template>
  <div class="main">
    <div class="main-content">
      <div class="main-content-scroll">
        <h2>添加试题</h2>
        <div class="main-layout-content">
          题目信息
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: 'addTestQuestions'
    }
</script>

<style scoped lang="scss">
  @import "../../assets/scss/common";

  .main {
    @include whall;

    .main-content {
      @include whall;
      overflow-y: scroll;

      &::-webkit-scrollbar {
        display: none;
      }

      .main-content-scroll {
        @include wall;
        display: flex;
        flex-direction: column;

        h2 {
          padding: 20px 0;
          margin: 10px 0;
          font-size: 22px;
          font-weight: normal;
        }

        .main-layout-content {
          @include wall;
          background: rgb(255, 255, 255);
          padding: 24px;
          margin: 0px 0px 20px;
          border-radius: 10px;
        }
      }
    }
  }
</style>