<template>
  <div>

    <HeroSection />

    <div class="articles">

      <ArticleCard
          v-for="article in articles"
          :key="article.id"
          :article="article"
      />

    </div>

  </div>
</template>

<script setup>
import HeroSection from '../components/HeroSection.vue'
import ArticleCard from '../components/ArticleCard.vue'
import articles from '../data/articles'
</script>
