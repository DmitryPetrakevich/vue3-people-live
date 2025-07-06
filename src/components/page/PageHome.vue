<template>
    <main class="list-articles">
    <div class="list-articles__container">
      <div class="list-articles__list">

        <CardArticle 
        v-for="(item) in newsList"
        :key="item.id"
        class="list-articles__card card-article" 
        :title="item.title"
        :description="item.description"
        />


      </div>
    </div>
  </main>
  
</template>

<script>
import CardArticle from '@/components/card/CardArticle.vue';
import newsList from "@/json/news.json";
export default {
  components: {
    CardArticle,
  },
  data() {
    return {
      newsList: newsList,
    };
  },
};
</script>

<style lang="less">

.list-articles {
  &__container {
    .container();
    padding-top: 75px;
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