<template>
          <div class="list-articles__card card-article">
          <h4 class="card-article__title">
            {{ title }}
          </h4>

          <p class="card-article__description">
            {{ description }}
          </p>
        </div>
  
</template>

<script>
export default {
  name: "CardArticle",
  props: {
    title: {
      type: String,
      default: ""
    },
    description: {
      type: String,
      default: ""
    }
  }
}
</script>

<style lang="less">
.list-articles {
  &__container {
    .container();
  }
  &__card {
    margin-bottom: 15px;
  }
}

.card-article {
  box-sizing: border-box;
  position: relative;
  padding: 20px 30px 20px 15px;
  box-shadow: 0 0 5px 1px @brown;
  background-color: @white;

  &__title {
    margin: 0 0 10px;
    color: @light_orange;
    font-size: 20px;
    cursor: pointer;
  }

  &__description {
    margin: 0 0 10px;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;

    &:last-child {
      margin-bottom: 0;
    }
  }
}
</style>