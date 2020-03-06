<template>
  <div class="app-page create-topic-page">
    <div class="page-form-container">
      <h1 class="page-form-title">
        新话题
      </h1>
      <topic-form :category-slug="$route.params.categorySlug"/>
    </div>
  </div>
</template>

<script>
import TopicForm from '@/components/TopicForm'

export default {
  components: { TopicForm }
}
</script>

<style lang="stylus" scoped>
</style>
