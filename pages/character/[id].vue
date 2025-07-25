<template>
  <PageContainer>
    <div class="flex gap-16">
      <img :src="data.image" width="369" height="461" class="rounded-2xl" />

      <div class="flex flex-col gap-12">
        <h1 class="text-5xl">{{ data.name }}</h1>

        <p>Praticou de {{ data.episode.length }} episódios</p>

        <div class="flex gap-6">
          <p>{{ data.status === "Alive" ? "Vivo" : "Morto" }}</p>
          <p>{{ data.species }}</p>
          <p>{{ data.gender }}</p>
        </div>
      </div>
    </div>
  </PageContainer>
</template>

<script setup>
const route = useRoute();

const { id } = route.params;

const { data } = await useFetch(
  `https://rickandmortyapi.com/api/character/${id}`
);

useHead({
  title: `${data.value.name} - Rick And Morty`,
  link: [{ rel: "icon", type: "image/x-icon", href: data.value.image }]
});
</script>
