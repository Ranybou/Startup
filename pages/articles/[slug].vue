<script setup>
const query = gql`
  query article($slug: String!) {
    article(where: { slug: $slug }) {
      titre
      texte {
        html
      }
    }
  }
`;

const article = ref();

const route = useRoute();
const { data } = await useAsyncQuery(query, {
  slug: route.params.slug,
});

console.log(data.value);
article.value = data.value.article;
</script>

<template>
  <div v-if="article" class="max-w-lg">
    <h2 class="text-3xl text-center">{{ article.titre }}</h2>
    <div v-html="article.texte.html"></div>
  </div>
  <div v-else>
    <li>Loading...</li>
  </div>
</template>
