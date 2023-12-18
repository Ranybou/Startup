<script setup>
const query = gql`
  query Articles {
    articles {
      createdAt
      publishedAt
      titre
      slug
      updatedAt
      image {
        url(transformation: { document: { output: { format: webp } } })
      }
    }
  }
`;

const articles = ref();
const { data } = await useAsyncQuery(query);

console.log(data.value);
articles.value = data.value.articles;
</script>

<template>
  <li v-for="article in articles" class="list-none">
    <NuxtLink :to="`/articles/${article.slug}`">
      <h2>
        {{ article.titre }}
      </h2>
      <NuxtImg :src="article.image.url" :alt="article.titre" />
    </NuxtLink>
  </li>
</template>
