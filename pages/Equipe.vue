<script setup>
const query = gql`
  query Equipe {
    page(where: { slug: "equipe" }) {
      slug
      titre
      texte {
        html
      }
    }
  }
`;

const equipe = ref();
const { data } = await useAsyncQuery(query);
console.log(data.value);
equipe.value = data.value.page;
</script>

<template>


  <div class="text-xl text-center" v-html="equipe.texte.html" ></div>

</template>
