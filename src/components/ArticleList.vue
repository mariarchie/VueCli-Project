<template>
  <div>
    <ul>
      <li v-for="article in articles" :key="article.title">
        <h2>{{ article.title }}</h2>
        <p>{{ article.content }}</p>
        <ul>
          <li v-for="tag in article.tags" :key="tag">{{ tag }}</li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    articles: {
      type: Array,
      required: true
    }
  }
};
</script>
