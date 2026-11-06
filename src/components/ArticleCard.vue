<template>
  <div class="card">
    <img :src="article.image" alt="Article Image" />

    <h3>{{ article.title }}</h3>

    <p><strong>Author:</strong> {{ article.author }}</p>

    <p>{{ article.summary }}</p>

    <RouterLink :to="'/article/' + article.id">
      Read More
    </RouterLink>
  </div>
</template>

<script setup>
defineProps({
  article: Object
})
</script>

<style scoped>
.card{
  width:250px;
  background:#eee;
  padding:10px;
  border-radius:8px;
}

img{
  width:100%;
}
</style>