<template>
  <div>

    <h1>{{ article?.title }}</h1>

    <p>
      <strong>Author:</strong>
      {{ article?.author }}
    </p>

    <p>{{ article?.summary }}</p>

  </div>
</template>

<script setup>
import { useRoute } from 'vue-router'
import articles from '../data/articles'

const route = useRoute()

const article = articles.find(
    item => item.id == route.params.id
)
</script>