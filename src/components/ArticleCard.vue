<template>
  <div class="article">
    <h2>{{ article.title }}</h2>
    <div class="content">
      <img :src="article.content.image" alt="Article Image">
      <p>Date: {{ article.content.date }}</p>
      <p>Category: {{ article.content.category }}</p>
      <p v-html="article.content.text"></p>
      <img :src="article.content.sloganImg" alt="Article Slogan Image">
      <h3>{{ article.content.secondTitle }}</h3>
      <p>{{ article.content.secondText }}</p>
      <ul>
        <li v-for="item in article.content.list" :key="item">{{ item }}</li>
      </ul>
      <img :src="article.content.secondImage" alt="Article Second Image">
      <p>{{ article.content.thirdText }}</p>
    </div>
  </div>
</template>
  
<script>
export default {
  props: {
    article: {
      type: Object,
      required: true
    }
  }
}
</script>
 
  