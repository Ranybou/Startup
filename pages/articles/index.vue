<script setup>
const query = gql`
query Articles {
  articles {
    createdAt
    publishedAt
    titre
    slug
    updatedAt
  }
}
`;

const articles = ref();
const { data } = await useAsyncQuery(query);

console.log(data.value);
articles.value = data.value.articles;
</script>

<template>
  <li v-for="article in articles">
    <NuxtLink :to="`/articles/${article.slug}`">
      <h2>
        {{ article.titre }}
      </h2>

      <div v-html="produit.texte.html"></div>
    </NuxtLink>
  </li>
</template>
