<template>
  <section class="flex flex-col gap-8 items-center xl:items-start">
    <ListingHeader title="Episódios" />

    <div
      class="flex gap-4 flex-wrap justify-center lg:grid lg:grid-cols-[repeat(5,1fr)]"
    >
      <Card
        v-for="currentEpisode of data.results"
        class="flex flex-col gap-2 justify-between min-h-[150px] max-w-[250px]"
      >
        <div class="flex gap-2 items-center">
          <IconsPlay class="flex-[0_0_24px]" />

          <p>{{ currentEpisode.name }} | {{ currentEpisode.episode }}</p>
        </div>

        <div class="flex items-center justify-between">
          <SeeDocumentDetails class="my-auto" />

          <IconsHeartFilled :width="32" :height="32" />
        </div>
      </Card>
    </div>
  </section>
</template>

<script setup>
import Card from "@/components/Card/index.vue";
import ListingHeader from "@/components/ListingHeader/index.vue";
import SeeDocumentDetails from "@/components/SeeDocumentDetails/index.vue";

const { data, status, error, refresh, clear } = await useFetch(
  "https://rickandmortyapi.com/api/episode"
);
</script>
